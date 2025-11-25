# Maria Garcia Iglesias Portfolio - Style Guide

## Overview
This style guide defines the design system for the Maria Garcia Iglesias portfolio website. It ensures consistency across all pages and provides clear guidelines for future development.

## Design Principles

### 1. Accessibility First
- Maintain WCAG 2.1 AA compliance
- Ensure sufficient color contrast (minimum 4.5:1 for normal text)
- Provide semantic HTML structure
- Include proper ARIA labels where needed

### 2. Mobile-First Responsive Design
- Design for mobile devices first, then scale up
- Use flexible layouts and relative units
- Ensure touch-friendly interactive elements (minimum 44x44px)

### 3. Performance
- Minimize external dependencies
- Optimize images and assets
- Use modern CSS instead of inline styles
- Lazy load non-critical resources

### 4. Clean & Professional
- Minimal, focused design
- Clear visual hierarchy
- Consistent spacing and alignment
- Professional typography

---

## Color Palette

### Primary Colors
```css
--color-primary-black: #000000;      /* Headings, site title */
--color-primary-gray: #3f3f3f;       /* Body text */
--color-white: #ffffff;              /* Backgrounds, light text */
```

### Secondary Colors
```css
--color-gray-light: #dbdbdb;         /* Borders, dividers */
--color-gray-lightest: #f2f2f2;      /* Section backgrounds */
--color-gray-medium: #4f4f4e;        /* Icons, secondary elements */
```

### Accent Colors
```css
--color-accent-blue: #3b526d;        /* Form labels, links */
--color-accent-error: #ff2825;       /* Error states, validation */
```

### Usage Guidelines
- Use `--color-primary-black` for all headings and emphasized text
- Use `--color-primary-gray` for body text and paragraphs
- Background should be white by default with `--color-gray-lightest` for alternate sections
- Maintain 4.5:1 contrast ratio for text readability

---

## Typography

### Font Families
```css
--font-primary: 'Arial', sans-serif;          /* Body text, headings */
--font-accent: 'Amaranth', sans-serif;        /* Navigation, buttons */
--font-secondary: 'Cabin', sans-serif;        /* Hero sections */
--font-quote: 'Georgia', serif;               /* Blockquotes */
```

### Font Sizes & Hierarchy

#### Desktop (min-width: 767px)
```css
--font-size-hero: 72px;              /* Hero headlines */
--font-size-h1: 40px;                /* Page titles */
--font-size-h2: 40px;                /* Section headings */
--font-size-h3: 28px;                /* Site title/brand */
--font-size-body: 20px;              /* Body text */
--font-size-nav: 16px;               /* Navigation items */
--font-size-small: 14px;             /* Footer, captions */
--font-size-caption: 12px;           /* Fine print */
```

#### Mobile (max-width: 766px)
```css
--font-size-hero: 48px;
--font-size-h1: 32px;
--font-size-h2: 28px;
--font-size-h3: 24px;
--font-size-body: 16px;
--font-size-nav: 14px;
--font-size-small: 12px;
--font-size-caption: 10px;
```

### Line Heights
```css
--line-height-tight: 1.2;            /* Headings */
--line-height-normal: 1.3;           /* Body text (26px/20px) */
--line-height-relaxed: 1.9;          /* Quotes (31px/16px) */
```

### Letter Spacing
```css
--letter-spacing-wide: 1px;          /* H2 headings */
--letter-spacing-normal: 0px;        /* Body text */
```

### Text Transforms
- **Site Title**: UPPERCASE
- **Navigation**: UPPERCASE
- **Body Text**: Normal case
- **Buttons**: Normal case with italic style

### Font Weights
- **Normal**: 400 (default for body text)
- **Medium**: 500 (for emphasis)
- **Bold**: 700 (for strong emphasis)

### Typography Best Practices
1. Never use more than 3 font families on a page
2. Maintain consistent line-height for readability
3. Use letter-spacing sparingly for uppercase text
4. Ensure text is scalable and responsive
5. Set a maximum line length of 75 characters for readability

---

## Spacing & Layout

### Spacing Scale
```css
--spacing-xs: 4px;
--spacing-sm: 8px;
--spacing-md: 16px;
--spacing-lg: 24px;
--spacing-xl: 32px;
--spacing-2xl: 48px;
--spacing-3xl: 64px;
```

### Container Widths
```css
--container-max-width: 1200px;
--container-narrow: 800px;
--container-padding: 16px;
```

### Layout Guidelines
1. Use consistent padding within containers (16px mobile, 24px desktop)
2. Maintain vertical rhythm with multiples of 8px
3. Use flexbox or grid for complex layouts
4. Ensure content doesn't touch screen edges on mobile
5. Center main content with max-width containers

---

## Components

### Navigation

#### Desktop Navigation
- Font: Amaranth, 16px, UPPERCASE
- Color: Inherits from theme
- Hover state: Visual feedback required
- Spacing: Consistent padding between items

#### Mobile Navigation
- Hamburger menu icon (22x15px)
- Full-screen overlay navigation
- Close button clearly visible
- Touch-friendly tap targets (minimum 44px)

#### Best Practices
- Keep navigation items to 5-7 maximum
- Use "More..." dropdown for additional items
- Ensure current page is visually indicated
- Provide clear hover/active states

### Buttons

#### Primary Button
```css
font-family: Amaranth;
font-style: italic;
padding: 12px 24px;
border-radius: 2px;
min-height: 44px;
```

#### States
- Default: Clear styling with good contrast
- Hover: Visual feedback (darker/lighter)
- Active: Pressed state indication
- Disabled: Reduced opacity (0.5)

### Forms

#### Input Fields
```css
border: 1px solid #dbdbdb;
padding: 8px;
border-radius: 2px;
font-size: 16px; /* Prevents iOS zoom */
```

#### Labels
```css
font-size: 90% of base;
color: #3b526d;
margin-bottom: 8px;
```

#### Error States
```css
border-color: #ff2825;
error-text-color: #ff2825;
```

#### Best Practices
- Always include visible labels
- Use placeholder text sparingly
- Provide clear error messages
- Ensure mobile keyboard optimization
- Add autocomplete attributes

### Cards & Sections

#### Section Spacing
- Padding: 48px 0 (desktop), 32px 0 (mobile)
- Alternating backgrounds (white/light gray)

#### Card Style
```css
background: white;
box-shadow: 0 2px 8px rgba(0,0,0,0.1);
border-radius: 4px;
padding: 24px;
```

### Hero/Banner Section

#### Specifications
- Minimum height: 400px (desktop), 300px (mobile)
- Background: Image with overlay if needed
- Text color: White (#ffffff)
- Centered content
- Background-size: cover
- Background-position: center

#### Content Guidelines
- Large headline (72px desktop, 48px mobile)
- Short subtitle (12px)
- Optional CTA button
- Ensure text readability with overlay if needed

### Blockquotes

```css
font-family: Georgia, serif;
font-style: italic;
font-size: 16px;
line-height: 31px;
padding-left: 24px;
border-left: 4px solid #dbdbdb;
color: #3f3f3f;
```

---

## Icons & Graphics

### Icon Specifications
- Size: 20x20px (default), 22x15px (hamburger)
- Color: currentColor (inherits from parent)
- Stroke width: 1px-1.6px
- Style: Outline/line-based icons

### SVG Best Practices
1. Use inline SVG for icons that need styling
2. Remove unnecessary metadata from SVG files
3. Use currentColor for fill/stroke to inherit text color
4. Provide viewBox for proper scaling
5. Include title element for accessibility

### Image Guidelines
- Use WebP format with fallback to JPEG/PNG
- Optimize images before upload (max 200KB for photos)
- Use srcset for responsive images
- Include descriptive alt text for all images
- Lazy load images below the fold

---

## Accessibility Standards

### Semantic HTML
- Use proper heading hierarchy (h1 > h2 > h3)
- Use `<nav>` for navigation
- Use `<main>` for main content
- Use `<article>` and `<section>` appropriately
- Use `<button>` for interactive elements

### ARIA Labels
- Provide `aria-label` for icon-only buttons
- Use `aria-current="page"` for current navigation item
- Add `role="navigation"` where appropriate
- Use `aria-expanded` for expandable menus

### Keyboard Navigation
- All interactive elements must be keyboard accessible
- Provide visible focus indicators
- Ensure logical tab order
- Support ESC key to close modals/menus

### Color Contrast
- Body text: 4.5:1 minimum (#3f3f3f on #ffffff = 9.73:1) ✓
- Large text (18pt+): 3:1 minimum
- UI components: 3:1 minimum
- Test all color combinations

### Screen Reader Support
- Provide descriptive link text (avoid "click here")
- Use alt text for images
- Hide decorative elements from screen readers
- Provide skip navigation links

---

## Responsive Design

### Breakpoints
```css
/* Mobile First */
--breakpoint-sm: 576px;   /* Small tablets */
--breakpoint-md: 767px;   /* Tablets */
--breakpoint-lg: 1024px;  /* Desktop */
--breakpoint-xl: 1200px;  /* Large desktop */
```

### Mobile Optimizations
- Touch-friendly targets (44x44px minimum)
- Hamburger menu navigation
- Stacked layouts
- Reduced font sizes
- Optimized images

### Desktop Enhancements
- Multi-column layouts
- Hover effects
- Larger typography
- Expanded navigation
- Enhanced spacing

---

## Code Standards

### HTML Best Practices
1. Use HTML5 doctype: `<!DOCTYPE html>`
2. Include proper meta tags (charset, viewport)
3. Use semantic HTML elements
4. Avoid inline styles (use CSS classes)
5. Keep HTML structure clean and indented
6. Close all tags properly
7. Use lowercase for tags and attributes
8. Include alt attributes on images

### CSS Best Practices
1. Use external stylesheets (not inline or embedded)
2. Follow BEM or similar naming convention
3. Use CSS variables for consistency
4. Mobile-first media queries
5. Group related styles together
6. Comment complex CSS
7. Avoid !important unless necessary
8. Use shorthand properties where appropriate

### JavaScript Best Practices
1. Place scripts at end of body or use defer
2. Minimize inline JavaScript
3. Use event delegation for performance
4. Ensure progressive enhancement
5. Test without JavaScript enabled
6. Use modern ES6+ features
7. Comment complex logic

### File Organization
```
/
├── index.html
├── about.html
├── css/
│   ├── main.css
│   └── responsive.css
├── js/
│   └── main.js
├── images/
│   ├── hero-bg.jpg
│   └── [optimized images]
├── fonts/
│   └── [web fonts if needed]
└── styleguide.md
```

---

## Performance Guidelines

### Page Load Optimization
- Target: < 3 seconds on 3G connection
- Minimize HTTP requests
- Compress and minify CSS/JS
- Use browser caching
- Defer non-critical resources

### Image Optimization
- Compress images (80-85% quality)
- Use appropriate formats (WebP, JPEG, PNG)
- Implement lazy loading
- Use responsive images with srcset
- Provide appropriate dimensions

### CSS Optimization
- Remove unused CSS
- Combine stylesheets where possible
- Use CSS instead of images for simple graphics
- Minimize specificity conflicts

### JavaScript Optimization
- Remove unused JavaScript
- Defer non-critical scripts
- Use async/defer attributes
- Minimize DOM manipulation

---

## Browser Support

### Target Browsers
- Chrome (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)
- Edge (last 2 versions)
- Mobile Safari (iOS 12+)
- Chrome Mobile (Android 8+)

### Progressive Enhancement
1. Build core functionality with HTML
2. Enhance with CSS
3. Add JavaScript for interactivity
4. Test without JavaScript
5. Provide fallbacks for older browsers

---

## Content Guidelines

### Writing Style
- Use clear, concise language
- Write in active voice
- Keep sentences short (15-20 words)
- Use proper grammar and punctuation
- Proofread all content

### Formatting
- Use headings to structure content
- Break text into scannable paragraphs
- Use bulleted lists for multiple points
- Highlight important information
- Include relevant quotes or testimonials

### SEO Best Practices
- Use descriptive page titles (50-60 characters)
- Write unique meta descriptions (150-160 characters)
- Include relevant keywords naturally
- Use proper heading hierarchy
- Add alt text to images
- Create descriptive URLs

---

## Maintenance & Updates

### Regular Checks
- Test all links (monthly)
- Update content regularly
- Check browser compatibility
- Review analytics
- Update dependencies
- Backup site files

### Version Control
- Use Git for version control
- Commit often with clear messages
- Tag releases
- Document changes
- Keep backup copies

---

## Resources

### Tools
- Browser DevTools for testing
- Lighthouse for performance audits
- WAVE for accessibility testing
- W3C Validator for HTML/CSS validation

### References
- MDN Web Docs
- W3C Standards
- WCAG Guidelines
- Google PageSpeed Insights

---

Last Updated: 2025-11-24
