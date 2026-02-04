# CV Website Improvements Summary

## Completed

### Accessibility
- **Added aria-labels to social media icons** - `index.md` and `resume.md` contact links
- **Enhanced focus styles** - Visible focus rings on all interactive elements (buttons, links, nav dots)
- **Semantic HTML landmarks** - `<main>`, `<nav>`, `<footer>` elements in layout
- **Decorative SVG hidden from screen readers** - `aria-hidden="true"` on all icon SVGs

### SEO & Social
- **Canonical URL** - `<link rel="canonical">` on all pages
- **Keywords meta tag** - Relevant data engineering terms
- **Open Graph tags** - `og:title`, `og:description`, `og:type`, `og:image`, `og:url`
- **Twitter Card tags** - `twitter:card`, `twitter:title`, `twitter:description`, `twitter:image`

### Mobile Experience
- **Card swipe UI** - Full-viewport scroll-snap cards on mobile
- **Navigation dots** - Fixed right-side dots with IntersectionObserver tracking
- **Touch support** - `touch-action: manipulation` on all buttons, peek indicators between cards

### Layout & Styling
- **Smooth scrolling** - `scroll-behavior: smooth` on html
- **Print layout** - Full print stylesheet: black/white colors, contact info repositioned top-right, URLs revealed, buttons hidden, page-break rules
- **Dark mode** - Manual toggle + system preference auto-detect, persisted to localStorage
- **Responsive typography** - Scaled headings and spacing at 768px and 480px breakpoints

### Performance
- **Resource preloading** - `<link rel="preload" as="style">` for `style.css`
- **Minified inline SVGs** - Removed redundant `xmlns` from all 9 inline SVGs across layout and content

### SEO (structured data)
- **JSON-LD Person schema** - Name, job title, employer, sameAs links, knowsAbout skills

### Code Quality
- **Removed CSS redundancy** - Duplicate rules consolidated
- **Consistent job header print styles** - Single set of flex/spacing rules

---

## Closed (assessed as N/A)

- **Favicon PNG/ICO fallbacks** — SVG favicon is already linked and universally supported by modern browsers. No action needed.
- **`loading=lazy` for SVG icons** — This attribute only applies to `<img>` and `<iframe>`. All icons are inline SVGs. There are no `<img>` tags on the site.
- **PDF download button** — No PDF file in source. Not needed.
- **Export options (JSON Resume, vCard)** — Not needed.
- **Security headers** — GitHub Pages does not support custom HTTP headers without a proxy.
- **Dependency updates** — Google Fonts is the only external dependency. No version pinning concerns.
- **CSS modularization** — The file is well-organized with clear section comments at ~1,400 lines. Splitting it requires either multiple HTTP requests (a net performance regression on a small site) or a Sass build pipeline that adds tooling complexity. Both tradeoffs only pay off for multi-developer projects or large shared component libraries. A single-person CV site does not justify the overhead.
- **JS modularization** — The theme init script must stay inline; it runs before `<body>` to prevent a flash of the wrong theme on load. The main script is ~90 lines of self-contained logic with no shared dependencies. Externalizing it adds an HTTP request for negligible gain. No module system, no imports, no reason to split.
- **Skills progress bars** — Skill proficiency is subjective and context-dependent. A percentage implies an objective, measurable rating that does not exist. Recruiters may screen out candidates who self-rate below an arbitrary threshold even when actual depth is strong. The skills table already communicates what technologies are known; depth and competence are demonstrated by the experience bullet points and quantified achievements. This is why LinkedIn moved away from skills ratings, and why industry-standard resumes list skills without scores.

---

## Future enhancements (larger scope, optional)

### Content
- Project portfolio — dedicated section with descriptions and links
- Interactive timeline — visual career progression

### Functionality
- Advanced filtering — filter experience by technology or industry
- Search — quick search within CV content
- Privacy-focused analytics — visitor engagement without third-party tracking

### Technical
- Service worker / PWA — offline support and installability
- Automated testing — link validation and rendering checks
- Multilingual support — language toggle

---

## File reference

| File | Role |
|------|------|
| `_layouts/default.html` | Shared layout: head, buttons, scripts, card nav |
| `assets/css/style.css` | All styles (themes, layout, responsive, print) |
| `index.md` | Full CV (5 cards) |
| `resume.md` | Condensed resume (4 cards) |
| `_config.yml` | Jekyll config, plugins |

---

*Last updated: February 4, 2026*
