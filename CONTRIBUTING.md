# 🤝 Contributing to Roey Zalta's Data Science Portfolio

Thank you for your interest in contributing to this data science portfolio! This document provides guidelines and instructions for potential collaborators who want to help improve the portfolio website.

[![GitHub Issues](https://img.shields.io/github/issues/roy2392/roy2392.github.io?style=flat-square)](https://github.com/roy2392/roy2392.github.io/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/roy2392/roy2392.github.io?style=flat-square)](https://github.com/roy2392/roy2392.github.io/pulls)
[![Contributors](https://img.shields.io/github/contributors/roy2392/roy2392.github.io?style=flat-square)](https://github.com/roy2392/roy2392.github.io/graphs/contributors)

---

## 📋 Table of Contents

- [🚀 Getting Started](#-getting-started)
- [🔧 Development Setup](#-development-setup)
- [📝 Contribution Guidelines](#-contribution-guidelines)
- [🎨 Code Style Guidelines](#-code-style-guidelines)
- [📊 Adding New Projects](#-adding-new-projects)
- [🖼️ Image Guidelines](#️-image-guidelines)
- [🔄 Pull Request Process](#-pull-request-process)
- [🐛 Bug Reports](#-bug-reports)
- [💡 Feature Requests](#-feature-requests)
- [📞 Getting Help](#-getting-help)

---

## 🚀 Getting Started

### Prerequisites

Before contributing, ensure you have:

- **Git** installed on your local machine
- A **GitHub account**
- A modern **text editor** (VS Code, Sublime Text, Atom, etc.)
- Basic knowledge of **HTML5**, **CSS3**, and **JavaScript**
- Understanding of **responsive web design** principles

### 🍴 Fork and Clone the Repository

1. **Fork the repository** by clicking the "Fork" button on the [main repository page](https://github.com/roy2392/roy2392.github.io)

2. **Clone your fork** to your local machine:
   ```bash
   git clone https://github.com/YOUR_USERNAME/roy2392.github.io.git
   cd roy2392.github.io
   ```

3. **Add the original repository as upstream**:
   ```bash
   git remote add upstream https://github.com/roy2392/roy2392.github.io.git
   ```

4. **Verify your remotes**:
   ```bash
   git remote -v
   # Should show:
   # origin    https://github.com/YOUR_USERNAME/roy2392.github.io.git (fetch)
   # origin    https://github.com/YOUR_USERNAME/roy2392.github.io.git (push)
   # upstream  https://github.com/roy2392/roy2392.github.io.git (fetch)
   # upstream  https://github.com/roy2392/roy2392.github.io.git (push)
   ```

---

## 🔧 Development Setup

### Local Development Environment

1. **Navigate to the project directory**:
   ```bash
   cd roy2392.github.io
   ```

2. **Start a local server** (recommended for testing):
   ```bash
   # Option 1: Python 3
   python -m http.server 8000
   
   # Option 2: Python 2
   python -m SimpleHTTPServer 8000
   
   # Option 3: Node.js (if you have it installed)
   npx http-server
   
   # Option 4: PHP (if available)
   php -S localhost:8000
   ```

3. **Open your browser** and navigate to:
   - `http://localhost:8000` (for most servers)
   - The portfolio should load with all functionality

### 📁 Project Structure Understanding

```
roy2392.github.io/
├── 📄 index.html              # Main portfolio page
├── 📄 README.md               # Project documentation
├── 📄 CONTRIBUTING.md         # This file
├── 📄 LICENSE.txt             # Creative Commons license
├── 📁 assets/                 # Static assets
│   ├── 📁 css/               # Stylesheets
│   │   ├── main.css          # Main stylesheet
│   │   ├── fontawesome-all.min.css
│   │   └── noscript.css      # No-JS fallback styles
│   ├── 📁 js/                # JavaScript files
│   │   ├── main.js           # Main functionality
│   │   ├── jquery.min.js     # jQuery library
│   │   └── [other JS files]  # Template utilities
│   ├── 📁 sass/              # SASS source files
│   └── 📁 webfonts/          # Font files
├── 📁 images/                # Project images and assets
└── 📄 [template files]       # HTML5 UP template files
```

---

## 📝 Contribution Guidelines

### Types of Contributions Welcome

- 🐛 **Bug fixes** - Fix broken links, layout issues, or functionality problems
- 🎨 **Design improvements** - Enhance visual appeal and user experience
- 📱 **Responsive design** - Improve mobile and tablet compatibility
- ⚡ **Performance optimizations** - Optimize images, code, and loading times
- 📚 **Documentation** - Improve README, add comments, or create guides
- 🔧 **Code refactoring** - Clean up code while maintaining functionality
- 🌐 **Accessibility** - Improve screen reader compatibility and WCAG compliance
- 🔍 **SEO improvements** - Enhance search engine optimization

### What NOT to Contribute

- ❌ **Personal project changes** - Don't modify Roey's personal project descriptions or links
- ❌ **Contact information** - Don't change personal contact details
- ❌ **Branding changes** - Don't alter the personal branding or professional image
- ❌ **Unrelated content** - Don't add content unrelated to data science or the portfolio theme

---

## 🎨 Code Style Guidelines

### HTML Guidelines

- **Use semantic HTML5 elements** (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`)
- **Maintain proper indentation** (2 spaces or 4 spaces consistently)
- **Use descriptive class names** following the existing naming convention
- **Include alt attributes** for all images
- **Validate HTML** using [W3C Markup Validator](https://validator.w3.org/)

```html
<!-- ✅ Good -->
<section class="project-showcase">
    <article class="project-card">
        <h2 class="project-title">Project Name</h2>
        <img src="images/project.jpg" alt="Project screenshot showing data visualization" />
    </article>
</section>

<!-- ❌ Avoid -->
<div class="stuff">
    <div class="thing">
        <h2>Project</h2>
        <img src="pic.jpg" />
    </div>
</div>
```

### CSS Guidelines

- **Follow the existing SASS structure** in `assets/sass/`
- **Use consistent naming conventions** (kebab-case for classes)
- **Maintain responsive design** with mobile-first approach
- **Use CSS custom properties** for consistent theming
- **Comment complex styles** for clarity

```css
/* ✅ Good */
.project-card {
    background: var(--card-background);
    border-radius: 8px;
    padding: 1.5rem;
    transition: transform 0.3s ease;
}

.project-card:hover {
    transform: translateY(-4px);
}

/* ❌ Avoid */
.card {
    background: #fff;
    padding: 20px;
}
```

### JavaScript Guidelines

- **Use modern ES6+ syntax** where appropriate
- **Maintain compatibility** with the existing jQuery codebase
- **Add comments** for complex functionality
- **Test thoroughly** across different browsers
- **Follow existing patterns** in `assets/js/main.js`

```javascript
// ✅ Good
const initializePortfolio = () => {
    // Initialize smooth scrolling
    $('.scrolly').scrolly({
        speed: 1000,
        offset: 50
    });
};

// ❌ Avoid
function init() {
    $('.scrolly').scrolly();
}
```

---

## 📊 Adding New Projects

If you're helping to add a new data science project to the portfolio, follow these guidelines:

### 1. Project Information Required

- **Project title** and brief description
- **GitHub repository link**
- **Technologies used** (Python libraries, tools, etc.)
- **Key features** or achievements
- **High-quality project image** (see image guidelines below)

### 2. HTML Structure

Add the new project following the existing pattern in `index.html`:

```html
<article>
    <header>
        <h2><a href="GITHUB_REPO_LINK">Project Title<br /></a></h2>
    </header>
    <a href="GITHUB_REPO_LINK" class="image fit">
        <img src="images/project-image.jpg" alt="Descriptive alt text" />
    </a>
    <p>Brief project description highlighting key technologies and achievements.</p>
    <ul class="actions special">
        <li><a href="GITHUB_REPO_LINK" class="button">VIEW PROJECT</a></li>
    </ul>
</article>
```

### 3. Update Documentation

- Add the project to the **README.md** file
- Include it in the **PORTFOLIO.md** documentation
- Update the **CHANGELOG.md** with the addition

---

## 🖼️ Image Guidelines

### Image Requirements

- **Format**: JPG or PNG (WebP for optimization)
- **Dimensions**: Minimum 800x600px for project images
- **File size**: Keep under 500KB per image
- **Quality**: High-quality, professional-looking images
- **Naming**: Use descriptive, kebab-case filenames

### Image Optimization

Before adding images:

1. **Compress images** using tools like:
   - [TinyPNG](https://tinypng.com/)
   - [ImageOptim](https://imageoptim.com/)
   - [Squoosh](https://squoosh.app/)

2. **Use appropriate dimensions**:
   - Featured project: 1200x800px
   - Regular projects: 800x600px
   - Profile images: 400x400px

3. **Add descriptive alt text** for accessibility

### Image Placement

- Place all images in the `images/` directory
- Use descriptive filenames: `project-name-screenshot.jpg`
- Update image references in HTML accordingly

---

## 🔄 Pull Request Process

### Before Submitting a Pull Request

1. **Sync with upstream**:
   ```bash
   git fetch upstream
   git checkout main
   git merge upstream/main
   ```

2. **Create a feature branch**:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/bug-description
   ```

3. **Make your changes** following the guidelines above

4. **Test thoroughly**:
   - Test on multiple browsers (Chrome, Firefox, Safari, Edge)
   - Test responsive design on different screen sizes
   - Validate HTML and CSS
   - Check for broken links

5. **Commit your changes**:
   ```bash
   git add .
   git commit -m "feat: add responsive navigation menu
   
   - Implement mobile-friendly hamburger menu
   - Add smooth transitions and animations
   - Ensure accessibility compliance
   - Test across multiple devices"
   ```

### Commit Message Guidelines

Use conventional commit format:

- `feat:` - New features
- `fix:` - Bug fixes
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, etc.)
- `refactor:` - Code refactoring
- `perf:` - Performance improvements
- `test:` - Adding or updating tests

### Submitting the Pull Request

1. **Push your branch**:
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Create a Pull Request** on GitHub with:
   - **Clear title** describing the change
   - **Detailed description** of what was changed and why
   - **Screenshots** for visual changes
   - **Testing notes** describing how you tested the changes

3. **Pull Request Template**:
   ```markdown
   ## Description
   Brief description of changes made.
   
   ## Type of Change
   - [ ] Bug fix
   - [ ] New feature
   - [ ] Documentation update
   - [ ] Performance improvement
   - [ ] Code refactoring
   
   ## Testing
   - [ ] Tested on Chrome
   - [ ] Tested on Firefox
   - [ ] Tested on mobile devices
   - [ ] Validated HTML/CSS
   - [ ] Checked accessibility
   
   ## Screenshots (if applicable)
   Add screenshots of visual changes.
   
   ## Additional Notes
   Any additional information or context.
   ```

---

## 🐛 Bug Reports

### Before Reporting a Bug

1. **Check existing issues** to avoid duplicates
2. **Test in multiple browsers** to confirm the issue
3. **Clear browser cache** and test again

### Bug Report Template

When reporting bugs, please include:

```markdown
**Bug Description**
A clear description of what the bug is.

**Steps to Reproduce**
1. Go to '...'
2. Click on '...'
3. Scroll down to '...'
4. See error

**Expected Behavior**
What you expected to happen.

**Actual Behavior**
What actually happened.

**Screenshots**
If applicable, add screenshots.

**Environment**
- Browser: [e.g., Chrome 91.0]
- OS: [e.g., macOS 11.4]
- Device: [e.g., iPhone 12, Desktop]
- Screen size: [e.g., 1920x1080]

**Additional Context**
Any other context about the problem.
```

---

## 💡 Feature Requests

### Feature Request Template

```markdown
**Feature Description**
A clear description of the feature you'd like to see.

**Problem Statement**
What problem would this feature solve?

**Proposed Solution**
How do you envision this feature working?

**Alternatives Considered**
Any alternative solutions you've considered.

**Additional Context**
Screenshots, mockups, or examples that help explain the feature.

**Priority**
- [ ] Low
- [ ] Medium
- [ ] High
- [ ] Critical
```

---

## 📞 Getting Help

### Communication Channels

- **GitHub Issues**: For bugs, features, and general questions
- **Email**: [roey.zalta@gmail.com](mailto:roey.zalta@gmail.com) for direct communication
- **LinkedIn**: [Roey Zalta](https://www.linkedin.com/in/roey-zalta-965246167/) for professional inquiries

### Resources

- **HTML5 UP Documentation**: [html5up.net](https://html5up.net/)
- **MDN Web Docs**: [developer.mozilla.org](https://developer.mozilla.org/)
- **GitHub Pages Documentation**: [docs.github.com/pages](https://docs.github.com/en/pages)
- **Accessibility Guidelines**: [webaim.org](https://webaim.org/)

---

## 🏆 Recognition

Contributors will be:

- **Listed in the README.md** contributors section
- **Mentioned in CHANGELOG.md** for significant contributions
- **Credited in commit messages** and pull request descriptions
- **Thanked personally** for their valuable contributions

---

## 📄 License

By contributing to this project, you agree that your contributions will be licensed under the same [Creative Commons Attribution 3.0 Unported License](LICENSE.txt) that covers the project.

---

<div align="center">

### 🙏 Thank You for Contributing!

Your contributions help make this portfolio better for everyone. Whether it's a small bug fix or a major feature, every contribution is valued and appreciated.

[![Contributors](https://img.shields.io/github/contributors/roy2392/roy2392.github.io?style=for-the-badge)](https://github.com/roy2392/roy2392.github.io/graphs/contributors)

**Happy Contributing! 🚀**

</div>
