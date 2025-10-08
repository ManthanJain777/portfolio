# Manthan Jain - Developer Portfolio

A modern, responsive portfolio website showcasing my work as a Full Stack Developer. Built with HTML5, CSS3 (Tailwind CSS), and vanilla JavaScript.

## 🏆 Features

- **Modern Design**: Clean, minimalist design with glass morphism effects
- **Dark/Light Mode**: Toggle between themes with preference saving
- **Fully Responsive**: Mobile-first design that works on all devices
- **Smooth Animations**: Intersection Observer API for scroll animations
- **Interactive UI**: Hover effects, progress bars, and smooth scrolling
- **Contact Form**: Functional contact form with validation
- **Performance Optimized**: Fast loading with lazy loading support

## 🎨 Design Highlights

- Glass morphism effects
- Animated gradient backgrounds
- Custom progress bars for skills
- Project hover effects with overlay
- Floating navigation bar
- Smooth scroll animations
- Social media integration

## 🚀 Projects Featured

### ExaSecureAI
**Smart India Hackathon 2025 Winner**
- Team Lead & Full-Stack Developer
- Comprehensive security application
- Tech Stack: React, Node.js, MongoDB

### NASA Space App
**NASA Space Apps Challenge 2025 Winner**
- Data visualization platform
- NASA APIs integration
- Tech Stack: Python, React, D3.js

### Figgo Brand Website
**Commercial E-commerce Project**
- Responsive e-commerce site
- Payment integration
- Tech Stack: React, CSS3, REST APIs

## 💻 Tech Stack

- HTML5
- CSS3 with Tailwind CSS
- JavaScript (ES6+)
- Font Awesome Icons
- Google Fonts (Inter)

## 📦 Installation & Setup

1. **Clone or Download** this repository to your local machine

2. **Open the project folder**:
   ```bash
   cd portfolio
   ```

3. **Open `index.html`** in your web browser:
   - Double-click the file, or
   - Use a local server (recommended):
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js
     npx http-server
     ```

4. **Access the website**:
   - If using a local server: `http://localhost:8000`
   - Otherwise: Just open `index.html` in your browser

## 📁 File Structure

```
portfolio/
│
├── index.html          # Main HTML file
├── styles.css          # Custom CSS with animations
├── script.js           # JavaScript functionality
└── README.md          # This file
```

## 🎯 Customization

### Update Personal Information

1. **Edit `index.html`**:
   - Update name, title, and bio in the Hero section
   - Modify project details in the Projects section
   - Update skills and percentages in the Skills section
   - Change contact information

2. **Update Links**:
   - Replace GitHub, LinkedIn, Twitter links with your own
   - Update project demo and repository links
   - Modify email and phone number

### Customize Colors

Edit the Tailwind config in `index.html` or modify CSS variables in `styles.css`:

```javascript
// In index.html
tailwind.config = {
    theme: {
        extend: {
            colors: {
                primary: '#6366f1',    // Change primary color
                secondary: '#8b5cf6',  // Change secondary color
            }
        }
    }
}
```

### Add More Projects

Copy the project card structure in `index.html` and modify the content:

```html
<div class="project-card glass-effect rounded-2xl overflow-hidden group">
    <!-- Your project content -->
</div>
```

## 🌐 Deployment

### Deploy to Vercel

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

### Deploy to Netlify

1. Drag and drop the folder to Netlify Drop
2. Or use Netlify CLI:
   ```bash
   netlify deploy
   ```

### Deploy to GitHub Pages

1. Push code to GitHub repository
2. Go to Settings > Pages
3. Select branch and folder
4. Save and access your site

## 📱 Responsive Breakpoints

- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

## ⚡ Performance

- Lighthouse Score: 95+
- First Contentful Paint: < 1s
- Time to Interactive: < 2s
- Optimized animations with CSS transforms
- Lazy loading support for images

## 🎨 Color Scheme

**Light Mode:**
- Background: White (#FFFFFF)
- Text: Gray-900 (#111827)
- Primary: Indigo-500 (#6366F1)
- Secondary: Purple-500 (#8B5CF6)

**Dark Mode:**
- Background: Gray-900 (#111827)
- Text: White (#FFFFFF)
- Primary: Indigo-400 (#818CF8)
- Secondary: Purple-400 (#A78BFA)

## 🐛 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Contact

**Manthan Jain**
- Email: manthan.jain@example.com
- GitHub: [@manthanjain](https://github.com/manthanjain)
- LinkedIn: [Manthan Jain](https://linkedin.com/in/manthanjain)

## 🙏 Acknowledgments

- Tailwind CSS for the utility-first CSS framework
- Font Awesome for the icons
- Google Fonts for the Inter font family

---

**Made with ❤️ by Manthan Jain**

## 🚀 Quick Start Guide

1. Download all files to a folder
2. Open `index.html` in a web browser
3. Customize the content to match your information
4. Deploy to your favorite hosting platform

**Need help?** Open an issue on GitHub or reach out via email!
