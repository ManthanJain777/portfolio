# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a **static portfolio website** for Manthan Jain, a Full Stack Developer. It's a single-page application built with vanilla HTML5, CSS3, and JavaScript (no build tools or frameworks required). The site features:

- Modern design with glass morphism effects
- Dark/Light theme toggle with localStorage persistence
- Responsive mobile-first design
- Smooth scroll animations using Intersection Observer API
- Featured projects: ExaSecureAI (SIH 2025 Winner), NASA Space App (NASA Winner), and Figgo Brand (E-commerce)

**Tech Stack:** HTML5, CSS3 (with Tailwind CDN for utility classes), Vanilla JavaScript (ES6+), Font Awesome Icons, Google Fonts (Inter)

## Common Development Commands

### Running the Portfolio Locally

Since this is a static site with no build process, you can run it directly:

```powershell
# Option 1: Using Python (if installed)
python -m http.server 8000
# Access at: http://localhost:8000

# Option 2: Using Node.js (if installed)
npx http-server
# Access at: http://localhost:8080

# Option 3: Just open the file directly
Start-Process "C:\Users\MY PC\portfolio\index.html"
```

### Deployment Commands

```powershell
# Deploy to Vercel (if Vercel CLI is installed)
vercel

# Deploy to Netlify (if Netlify CLI is installed)
netlify deploy

# For GitHub Pages: Push to GitHub and enable Pages in repository settings
git add .
git commit -m "Update portfolio"
git push origin main
```

### Development Workflow

```powershell
# Open project in VS Code
code "C:\Users\MY PC\portfolio"

# View git status and recent changes
git status
git log --oneline -10

# Test responsiveness - there's no specific command, but you can use browser dev tools
```

## Architecture & Code Structure

### File Organization

```
portfolio/
├── index.html          # Single-page HTML with all sections (Hero, About, Projects, Skills, Contact)
├── styles.css          # All CSS including animations, themes, and responsive design
├── script.js           # All JavaScript functionality
├── images/
│   └── myphoto.jpg    # Profile photo
└── README.md          # Project documentation
```

### Architecture Patterns

**Single-Page Application (SPA) with Vanilla JS:**
- **No framework or build system** - everything runs directly in the browser
- All sections (hero, about, projects, skills, contact) are in `index.html`
- Navigation uses anchor links (`#home`, `#about`, etc.) with smooth scrolling
- Theme state persisted in `localStorage`

**Theme System:**
- CSS custom properties (CSS variables) defined in `:root` in `styles.css`
- Two theme classes: `.dark-mode` and `.light-mode` toggle on `<body>`
- Theme preference stored in `localStorage` with key `'theme'`
- Default theme is dark mode

**Animation System:**
- Intersection Observer API tracks when sections enter viewport
- CSS animations defined in `@keyframes fadeIn`
- Classes like `.fade-in`, `.delay-1`, `.delay-2` applied dynamically
- Skill bars animate on scroll into view

**Navigation System:**
- Fixed navbar with glass morphism effect (backdrop blur)
- Adds `.scrolled` class when `window.scrollY > 50`
- Mobile menu toggles visibility of `.nav-links` with inline styles
- Smooth scroll behavior handled by JavaScript event listeners on anchor links

### Key JavaScript Components

**Location in `script.js`:**
- **Lines 1-29:** Theme toggle logic with localStorage persistence
- **Lines 31-42:** Navbar scroll effects and progress bar updates
- **Lines 44-57:** Smooth scrolling for anchor links (offset by 80px for navbar)
- **Lines 59-80:** Mobile menu toggle logic
- **Lines 82-98:** Contact form submission handler (prevents default, shows notification)
- **Lines 100-139:** Notification system (creates temporary toast notifications)
- **Lines 141-153:** Scroll progress bar (creates/updates width based on scroll position)
- **Lines 155-165:** Skill bar animation logic (resets width to 0, then animates to target)
- **Lines 167-187:** Intersection Observer setup for section animations
- **Lines 211-232:** Active navigation link highlighting based on scroll position

### CSS Architecture

**Location in `styles.css`:**
- **Lines 1-13:** CSS custom properties (`:root` variables for colors, transitions)
- **Lines 15-27:** Theme classes (`.dark-mode` and `.light-mode`)
- **Lines 52-140:** Navigation styles (fixed position, glass effect, responsive)
- **Lines 141-248:** Hero section with gradient background
- **Lines 272-328:** About section with grid layout and stats cards
- **Lines 329-426:** Project cards with hover effects and badges
- **Lines 427-476:** Skills section with animated progress bars
- **Lines 477-551:** Contact section with form styling
- **Lines 595-631:** Responsive breakpoints (992px, 768px)
- **Lines 633-656:** Animation keyframes and scroll progress bar

### Important Implementation Details

**Customization Points:**
- **Personal Information:** Edit `index.html` lines 38-49 (hero section) and 306-333 (contact info)
- **Projects:** Edit `index.html` lines 100-161 (project cards in grid)
- **Skills:** Edit `index.html` lines 174-292 (skill categories and percentages)
- **Colors:** Modify CSS variables in `styles.css` lines 1-13
- **Social Links:** Update `index.html` lines 45-48 and 373-376

**Form Handling:**
- Contact form currently shows a success notification but doesn't send emails
- To implement backend: Add form submission to external service (FormSpree, Netlify Forms, etc.)
- Form data logged to console (see `script.js` line 97)

**Theme Toggle Implementation:**
- Theme icon switches between `fa-moon` (dark mode) and `fa-sun` (light mode)
- Theme persists across page reloads via `localStorage.getItem('theme')`
- Body class toggles between `.dark-mode` and `.light-mode`

**Responsive Behavior:**
- Mobile menu appears at 768px breakpoint
- Grid layouts switch from 2-column to 1-column at 992px
- Navigation links hide on mobile, replaced by hamburger menu

## Development Guidelines

### When Modifying Code

**HTML Changes:**
- Maintain the section structure: `<section id="section-name">` for navigation to work
- Keep the `.container` wrapper for consistent width/padding
- Preserve class names used by JavaScript (e.g., `#themeToggle`, `#navbar`, `#contactForm`)

**CSS Changes:**
- Use CSS custom properties for colors/values to maintain theme consistency
- Follow the glass morphism pattern: `var(--glass)` background + `backdrop-filter: blur(10px)`
- Keep responsive breakpoints at 768px (mobile) and 992px (tablet)

**JavaScript Changes:**
- Theme toggle depends on localStorage key `'theme'` - don't change this
- Intersection Observer thresholds may need adjustment for different content lengths
- Mobile menu uses inline styles - consider refactoring to CSS classes for maintainability

### External Dependencies

**CDN Resources (loaded in `index.html`):**
- Google Fonts: Inter font family (lines 7-9)
- Font Awesome 6.4.0: Icons (line 10)
- Tailwind CSS: Not actually used - inline Tailwind config exists but styles are in `styles.css`

**No Package Manager:** This project has no `package.json`, no npm dependencies, and no build process.

## Contact Information

- **Developer:** Manthan Jain
- **Email:** jainmanthan289@gmail.com
- **GitHub:** [@ManthanJain777](https://github.com/ManthanJain777)
- **LinkedIn:** [manthan-jain-00542a33b](https://linkedin.com/in/manthan-jain-00542a33b)
- **Location:** Udaipur, India

## Performance Considerations

- Lighthouse score: 95+ (as documented in README)
- Images should be optimized before adding to `/images/`
- Current profile photo: `images/myphoto.jpg`
- Lazy loading supported but not currently implemented for images
- CSS animations use `transform` for GPU acceleration
