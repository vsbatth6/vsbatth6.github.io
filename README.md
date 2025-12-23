# Personal CV Website

A modern, responsive CV/resume website hosted on GitHub Pages with dark mode, mobile card navigation, and print optimization.

**Live site:** [vsbatth6.github.io](https://vsbatth6.github.io)

## Features

- **Dark/Light Mode** - Toggle button with system preference detection
- **PDF Download** - One-click resume download
- **Mobile Card UI** - Swipeable cards with navigation dots on mobile/tablet
- **Print Optimized** - Clean black & white print layout with proper page breaks
- **Multiple Themes** - Forest Green (active), Warm Charcoal, Professional Blue, and more
- **Responsive Design** - Adapts to desktop, tablet, and mobile
- **Accessibility** - Reduced motion support, keyboard navigation, focus styles

## File Structure

```
vsbatth6.github.io/
├── index.md                 # CV content (Markdown)
├── _config.yml              # Jekyll configuration
├── CNAME                    # Custom domain config
├── _layouts/
│   └── default.html         # HTML template with theme toggle & card nav JS
├── assets/
│   ├── css/
│   │   └── style.css        # All styles (organized by section)
│   └── virinderpal_batth_resume.pdf
└── README.md
```

## CV Structure (5 Cards)

| Card | Content |
|------|---------|
| 1 | Name, Title, Contact Links, Professional Summary |
| 2 | Experience: evolv Consulting (current) |
| 3 | Experience: USAA |
| 4 | Experience: HCL America |
| 5 | Technical Skills + Education |

## CSS Organization

The stylesheet is organized in this order:

1. CSS Reset & Base Styles
2. Color Schemes (themes)
3. Dark Mode Specific Overrides
4. Typography
5. Layout
6. Header Styles
7. Links
8. Horizontal Rules
9. Lists & Content
10. Experience Section
11. Tables
12. Key Achievements
13. Footer
14. Floating Buttons (theme toggle, PDF download)
15. Responsive Design
16. Mobile Card Swipe UI
17. Print Styles
18. Accessibility

## Customization

### Change Color Theme

Edit `assets/css/style.css` - uncomment your preferred theme in the COLOR SCHEMES section:

- Forest Green (active)
- Warm Charcoal
- Professional Blue
- Elegant Purple
- Midnight Blue

### Edit CV Content

Edit `index.md` using Markdown:

- `# Heading 1` - Name
- `## Heading 2` - Section titles
- `### Heading 3` - Job titles
- `**bold**` - Emphasis
- `- item` - Bullet points

### Print Settings

Print styles are configured for:
- 11pt body text, 20pt name, 16pt title
- Page break before Technical Skills (card 5)
- Black & white theme
- Contact info positioned top-right

## Local Development

```bash
# Install Jekyll
gem install bundler jekyll

# Run locally
bundle exec jekyll serve

# View at http://localhost:4000
```

## Deployment

Push to `main` branch - GitHub Pages auto-deploys within 1-2 minutes.

```bash
git add .
git commit -m "Update CV"
git push
```

## Tech Stack

- **Jekyll** - Static site generator
- **GitHub Pages** - Free hosting
- **CSS Custom Properties** - Theming
- **Intersection Observer** - Card navigation tracking
- **CSS Scroll Snap** - Mobile card swipe

---

Built with Jekyll and GitHub Pages
