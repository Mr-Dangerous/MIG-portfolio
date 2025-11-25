# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a modernized portfolio website for Maria Garcia Iglesias, a Spanish language teacher (K-4) at Hawthorne Elementary School in Teaneck, NJ. The site was migrated from Weebly to a clean, modern HTML/CSS implementation following web standards and accessibility best practices.

## Architecture

### Design System
The entire site is built on a centralized design system using CSS custom properties:
- **Single source of truth**: `css/style.css` contains all CSS variables for colors, typography, spacing, and layout
- **Mobile-first responsive design**: All breakpoints scale up from mobile (767px, 1024px)
- **Accessibility-focused**: WCAG 2.1 AA compliance with semantic HTML, ARIA labels, and keyboard navigation

### File Structure
```
/
├── index.html                    # Home page with Chinese proverb quote
├── about-me.html                 # Bio with profile photo
├── teaching-philosophy.html      # Educational philosophy
├── resume.html                   # Embedded Google Docs resume
├── intasc-standards.html        # Grid overview of 10 INTASC standards
├── standard-1.html through      # Individual standard pages with artifacts
│   standard-10.html
├── css/
│   └── style.css                # Shared stylesheet with CSS variables
├── assets/                      # Classroom photos for standard pages
│   ├── classroom_1.jpg
│   └── IMG_6330.jpg through IMG_6336.jpg
├── styleguide.md               # Complete design system documentation
└── CLAUDE.md                   # This file
```

### Page Template Structure
All HTML pages follow this consistent structure:
1. **Head**: Meta tags, Google Fonts (Amaranth, Cabin), link to `css/style.css`
2. **Header**: Sticky navigation with logo, hamburger menu (mobile), horizontal nav (desktop)
3. **Hero Section**: Full-width banner with background image and page title
4. **Main Content**: Centered container (max-width: 1200px) with semantic sections
5. **Footer**: Copyright information
6. **Navigation Script**: Mobile menu toggle with keyboard support (ESC to close)

## Key Implementation Details

### Navigation System
- **Desktop (>1024px)**: Horizontal navigation bar in header
- **Mobile (<1024px)**: Hamburger menu that slides in from left as full-screen overlay
- **Current page indicator**: Uses `aria-current="page"` with underline styling
- **Keyboard accessible**: Tab navigation, ESC key closes mobile menu

### INTASC Standards Pages (standard-1.html through standard-10.html)
Each standard page includes:
- **Hero image**: Uses one of 8 classroom photos from `assets/` folder (see image assignment below)
- **Standard Definition**: Official INTASC definition in highlighted box with blue accent border
- **Artifact Section**: Contains course metadata and content
  - **Standard 2**: Contains Maria's actual rationale about Polish Palm Sunday service experience
  - **Standards 1, 3-10**: Use lorem ipsum placeholders for artifact descriptions (ready for content to be added)
- **Back button**: Links to `intasc-standards.html`

### Image Assignment for Standards
- Standard 1: `assets/classroom_1.jpg`
- Standard 2: `assets/IMG_6330.jpg`
- Standard 3: `assets/IMG_6331.jpg`
- Standard 4: `assets/IMG_6332.jpg`
- Standard 5: `assets/IMG_6333.jpg`
- Standard 6: `assets/IMG_6334.jpg`
- Standard 7: `assets/IMG_6335.jpg`
- Standard 8: `assets/IMG_6336.jpg`
- Standard 9: `assets/classroom_1.jpg` (reused)
- Standard 10: `assets/IMG_6330.jpg` (reused)

### CSS Variables (Design Tokens)
All styling uses CSS custom properties defined in `:root`:
- **Colors**: `--color-primary-black`, `--color-primary-gray`, `--color-accent-blue`, etc.
- **Typography**: `--font-primary` (Arial), `--font-accent` (Amaranth), `--font-secondary` (Cabin)
- **Font sizes**: Mobile-first with desktop overrides at 767px breakpoint
- **Spacing**: 8px scale from `--spacing-xs` (4px) to `--spacing-3xl` (64px)
- **Layout**: `--container-max-width` (1200px), `--header-height` (70px)

### Accessibility Features
- Skip to main content link (`.sr-only` class)
- Semantic HTML5 elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`)
- ARIA labels on all buttons and navigation
- Focus states with `outline: 2px solid var(--color-accent-blue)`
- Reduced motion support: `@media (prefers-reduced-motion: reduce)`
- Color contrast ratios meet WCAG AA standards (body text: 9.73:1)

## Content Status & Next Steps

### Complete Pages
- Home (index.html)
- About Me with bio and photos
- Teaching Philosophy with full content
- Resume with embedded Google Docs
- INTASC Standards overview with grid layout
- All 10 individual standard pages with structure

### Pages Needing Content
The following INTASC standard pages have **lorem ipsum placeholders** that need to be replaced with actual artifact descriptions:
- standard-1.html (Learner Development)
- standard-3.html (Learning Environments)
- standard-4.html (Content Knowledge)
- standard-5.html (Application of Content)
- standard-6.html (Assessment)
- standard-7.html (Planning for Instruction)
- standard-8.html (Instructional Strategies)
- standard-9.html (Professional Learning)
- standard-10.html (Leadership and Collaboration)

Look for `<div class="artifact-section">` and replace the lorem ipsum `<p>` tags with Maria's actual artifact rationales and descriptions.

### Missing Pages
These pages were in the original Weebly site but haven't been created yet:
- self-assessment.html
- reflections.html (landing page)
- reflection-on-action-research-project.html
- reflection-as-language-teacher.html
- reflection-on-matl.html

When creating these pages, use the existing page templates (about-me.html or standard-1.html) as the base structure.

## Editing Guidelines

### When Adding Content to Standard Pages
1. Keep the standard definition unchanged (official INTASC text)
2. Replace lorem ipsum paragraphs with actual artifact descriptions
3. Maintain the existing HTML structure and classes
4. Include artifact metadata: course name, semester, ACTFL standards if applicable
5. Add links to external documents using the existing `.artifact-link` class

### When Creating New Pages
1. Copy an existing page that matches the content type (e.g., about-me.html for text content)
2. Update the `<title>` and meta description
3. Change hero background image (use classroom photos for standards-related content)
4. Update navigation `aria-current="page"` to mark the current page
5. Replace main content while maintaining semantic HTML structure
6. Keep the header, footer, and navigation script unchanged

### When Modifying Styles
- **Always edit `css/style.css`**, never add inline styles or page-specific stylesheets
- Use existing CSS variables rather than hard-coding values
- Follow mobile-first approach: base styles for mobile, `@media (min-width: 767px)` for tablet/desktop
- Test changes across all pages since they share the stylesheet
- Consult `styleguide.md` for design system specifications

## Important Notes

### Do NOT Modify
- The navigation JavaScript at the bottom of each page (unless fixing a bug)
- CSS variable names in `:root` (would break entire site)
- The header/footer structure (maintains consistency)
- Hero section gradient overlay formula: `linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3))`

### Original Content vs Generated Text
- **Standard 2 artifact**: Contains Maria's actual writing about the Polish Palm Sunday experience - preserve this
- **Lorem ipsum text**: Placeholder waiting for Maria's content - safe to replace
- **Standard definitions**: Official INTASC text - do not alter
- **About Me page**: Contains Maria's actual bio - preserve formatting and content

### External Dependencies
- Google Fonts (Amaranth, Cabin) - loaded via CDN with preconnect for performance
- Google Docs iframe in resume.html - embedded, not hosted locally
- All other assets are local (no jQuery, Bootstrap, or other frameworks)

## Reference Documentation

See `styleguide.md` for complete design system documentation including:
- Color palette with usage guidelines
- Typography hierarchy and font specifications
- Spacing scale and layout guidelines
- Component specifications (buttons, forms, cards)
- Accessibility standards and WCAG compliance details
- Performance optimization guidelines
- Browser support matrix
