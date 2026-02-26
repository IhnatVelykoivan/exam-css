# HTML+CSS Control Work (Dasteen Blog)

A responsive frontend developer blog template demonstrating modern HTML5 and CSS3 practices.

## Project Overview

This project implements a personal technology blog layout with focus on semantic markup, responsive design, and component-based CSS architecture. The design features a consistent lavender background (`#f0efff`) with purple accents (`#5956e9`).

## Technical Stack

- **HTML5**: Semantic elements, ARIA accessibility attributes, native dialog element
- **CSS3**: Flexbox, CSS Grid, Custom Properties, Media queries
- **Methodology**: BEM (Block Element Modifier)
- **Icons**: Inline SVG graphics for technology categories and social media
- **Interactivity**: Native HTML dialog element and scroll-based active nav tracking via JavaScript

## Project Structure

```
.
├── index.html                 # Main document with semantic structure
├── css/
│   └── style.css              # BEM-organized stylesheet (1115 lines)
├── images/
│   └── [27 image assets]      # Article thumbnails, avatar, hero photo, mailbox icon
└── README.md                  # Project documentation
```

## Implemented Components

### Header & Navigation

- Sticky header with white background
- Logo with purple dot accent
- Navigation links with underline hover/active effect
- Active link updates dynamically on scroll (JS `scroll` listener)
- "Buy the template" primary button
- Search button that opens modal dialog

### Hero Section

- Headline with line break for emphasis
- Descriptive paragraph about frontend development
- Email subscription form with input and submit button
- Developer portrait image; text and photo share equal width at desktop (50/50 flex split)

### Category Navigation

Five technology categories with colored SVG icons:

- **CSS** – Orange (`#ff6b35`) with CSS3 logo
- **JavaScript** – Gold (`#e8a000`) with JS logo
- **Tailwind** – Cyan (`#38bdf8`) with Tailwind logo (active state)
- **Vue.js** – Green (`#42b883`) with Vue logo
- **React.js** – Blue (`#0ea5e9`) with React logo

Grid layout: 2 equal columns on mobile (5th card centered), 5 equal columns on tablet and above.

### Article Grids

**Four distinct sections:**

1. **Featured Article** – Four equal mixed-category cards
2. **CSS Articles** – Four CSS tutorial cards
3. **JavaScript Articles** – Four JavaScript cards
4. **React.js Articles** – Four React cards

**Article Card Components:**

- Thumbnail image with scale hover effect
- Color-coded category tag
- Article title with link
- Author avatar, name, date, and read time
- Box shadow on hover with lift effect

### Search Dialog

- Native `<dialog>` element
- Backdrop with blur effect
- Search input with icon and close button
- Quick category links (CSS, JavaScript, Tailwind, Vue.js, React.js)
- Click outside to close functionality

### Subscribe Section

- Mailbox illustration centered
- Section title and subtitle
- Email input with placeholder
- Primary subscribe button
- Centered layout with max-width container

### Footer

- Dark background (`#111827`)
- Brand column with logo, tagline, and social media icons (Medium, Twitter, Instagram, LinkedIn)
- Four navigation columns:
  - Category links
  - About me links
  - Contact information (phone, email)
  - Follow us links
- Copyright notice

## Responsive Breakpoints

### Article Grids

| Breakpoint | Grid Columns | Navigation                    |
| ---------- | ------------ | ----------------------------- |
| < 480px    | 1 column     | Hidden (except logo and CTA)  |
| 480px+     | 2 columns    | Hidden                        |
| 768px+     | 2 columns    | Visible (desktop navigation)  |
| 1024px+    | 3 columns    | Visible                       |
| 1280px+    | 4 columns    | Visible                       |

### Category Cards

| Breakpoint | Grid Columns |
| ---------- | ------------ |
| < 768px    | 2 columns (5th card centered) |
| 768px+     | 5 columns (one equal row)     |

## Color System

### Brand Colors

- Primary Purple: `#5956e9` (buttons, active states, logo dot)
- Primary Dark: `#4340d4` (hover states)
- Primary Light: `#eeeeff` (background for interactive states)

### Category Tag Colors

- CSS: `#ff6b35`
- JavaScript: `#e8a000`
- HTML: `#e44d26`
- Tailwind: `#38bdf8`
- Vue.js: `#42b883`
- React.js: `#0ea5e9`
- UX: `#a855f7`
- UI: `#ec4899`

### Neutral Palette

- Page Background: `#f0efff` (lavender)
- Text Primary: `#1a1a2e`
- Text Muted: `#6b7280`
- Borders: `#e5e7eb`
- Footer Background: `#111827`
- Footer Text: `#d1d5db`

## Typography

- Base Font: Segoe UI, system-ui, -apple-system, sans-serif
- Type Scale: 12px, 14px, 16px, 18px, 24px, 32px, 40px
- Font Weights: 500 (medium), 600 (semi-bold), 700 (bold), 800 (extra-bold)

## Accessibility Features

- Semantic HTML5 elements (header, nav, main, section, article, footer)
- ARIA labels for icon-only buttons and interactive elements
- `aria-current="page"` on the active navigation link (updated dynamically)
- Focus visible indicators with purple outline
- Reduced motion media query support
- Proper heading hierarchy (h1 in hero, h2 for sections, h3 for cards)
- Alt text for all images
- Keyboard navigable dialog

## Interactive Elements

### Search Dialog Behavior

- Opens via JavaScript `showModal()` method
- Closes with close button, Escape key, or backdrop click
- Smooth fade-in animation
- Input automatically focused when opened

### Active Navigation

- Scroll listener checks which landmark section (`#hero`, `#categories`, `#about`) has passed the top of the viewport
- Applies `nav__link--active` class and `aria-current="page"` to the matching link
- Runs on page load and on every scroll event

### Card Interactions

- Hover: translateY(-4px) lift effect
- Shadow elevation from sm to md
- Image scale (1.04) on hover
- Cursor pointer on all clickable elements

## Browser Support

Tested on:

- Chrome (latest)
- Firefox (latest)

## Exam Requirements Fulfillment

- [X] Semantic HTML structure throughout
- [X] BEM methodology for all CSS classes
- [X] Responsive design with mobile-first approach
- [X] Interactive components (search dialog, active nav)
- [X] Modern CSS (Grid for layouts, Flex for components)
- [X] Custom properties for theming
- [X] Accessibility compliance (WCAG 2.1)
- [X] Clean, commented code organization
- [X] SVG icons for sharp rendering

## Development Notes

### CSS Architecture

- Mobile-first with progressive enhancement
- 1115 lines of organized CSS
- Custom properties at `:root` for easy theming
- No external dependencies
- Comments for each major section

### JavaScript Usage

- Two features: search dialog controls and active nav link tracking
- Native browser APIs only (`querySelectorAll`, `scroll` event, `classList`, `getBoundingClientRect`)
- No external libraries or frameworks

## Repository

- **URL**: https://github.com/IhnatVelykoivan/exam-css.git
- **Branch**: main
- **Commit**: cca4da0

---

**Exam Project – Frontend Development**
*Semantic HTML • BEM CSS • Responsive Design • Accessibility*
