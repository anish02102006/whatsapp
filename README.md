# Enginow Website - Task 3

## Overview

This is a professional, industry-standard multi-page website for Enginow built with pure HTML and CSS. The website has been enhanced through three iterations (Task 1, Task 2, and Task 3) to include full responsiveness, accessibility features, modern layout techniques, professional visual polish, and a comprehensive design system.

## Task 3 Enhancements

### 1. Reusable Component Library (Design System v1)
Created `components.css` with a dedicated component library including:
- **Buttons**: Primary and secondary button styles with hover effects
- **Cards**: Reusable card component with header, body, and footer sections
- **Badges/Tags**: Multiple tag variants (New, Trending, Popular, Primary, Success, Warning, Danger, Info)
- **Section Containers**: Consistent section spacing and layout utilities
- **Grid Layouts**: Responsive grid system (2, 3, 4 columns)
- **Social Icons**: Styled social media icon components
- **Testimonial Cards**: Specialized card design for testimonials with star ratings

### 2. Featured Courses Section on Home Page
- Beautiful card-based layout with tags (New, Trending, Popular)
- 3 featured courses displayed in responsive grid
- "Explore More Courses" CTA button
- Smooth fade-in animations
- Fully responsive design

### 3. Testimonials Section
- Added testimonials section with 3 student reviews
- Star ratings using emojis (⭐⭐⭐⭐⭐)
- Card-based layout with hover effects
- Responsive grid layout

### 4. Enhanced Footer
- **Quick Links**: Navigation to all pages
- **Social Media Icons**: Facebook, Twitter, LinkedIn, YouTube, Instagram (using emojis)
- **About Section**: Brief description of Enginow
- **Copyright Section**: Clean bottom section
- **Responsive Layout**: 3-column grid on desktop, single column on mobile

### 5. Improved Typography & Spacing
- **CSS Variables for Typography**: 
  - `--h1`, `--h2`, `--h3`, `--h4`, `--p`, `--small`
  - `--line-height-base`, `--line-height-heading`
- **Consistent Spacing**: Using CSS variables for all spacing
- **Professional Line Heights**: 1.6 for body text, 1.2 for headings
- **Fluid Typography**: Responsive font sizes using `clamp()`

### 6. Scroll to Top Button
- CSS-only implementation (no JavaScript)
- Fixed position at bottom right
- Smooth hover effects
- Accessible with ARIA labels
- Links to `#top` anchor

### 7. 404 Error Page
- Friendly, user-friendly error page
- Large 404 display with emoji illustration (🔍)
- Clear error message
- "Go Back Home" button
- Consistent design with rest of site
- Includes full navigation and footer

### 8. CSS Keyframe Animations
- **fadeIn**: Smooth fade-in animation
- **slideInLeft**: Slide in from left
- **slideInRight**: Slide in from right
- **gradientShift**: Animated gradient background
- **pulse**: Pulsing animation for emphasis
- Applied to hero section, cards, and sections

### 9. Enhanced Blog Page
- Updated to use new card component structure
- Tags added to blog posts (Trending, Popular, New)
- Improved layout with card header, body, and footer
- "Read More" buttons using secondary button style
- Responsive grid layout

### 10. Performance Optimizations
- Lazy loading ready (structure in place for images)
- Optimized CSS with component separation
- Efficient animations using CSS transforms
- Minimal CSS redundancy

## Project Structure

```
enginow-website/
│
├── index.html          # Home page with hero, featured courses, testimonials
├── courses.html        # Courses page with course cards
├── blog.html           # Blog page with article listings (enhanced layout)
├── about.html          # About page with vision and mission
├── contact.html         # Contact page with form
├── 404.html            # 404 error page
├── style.css            # Main stylesheet with CSS variables and animations
├── components.css       # Component library (Design System v1)
└── README.md            # This file
```

## Component Library Usage

### Buttons
```html
<a href="#" class="btn-primary">Primary Button</a>
<a href="#" class="btn-secondary">Secondary Button</a>
```

### Cards
```html
<article class="card">
    <div class="card-header">
        <h3>Card Title</h3>
    </div>
    <div class="card-body">
        <p>Card content</p>
    </div>
    <div class="card-footer">
        <a href="#" class="btn-primary">Action</a>
    </div>
</article>
```

### Tags/Badges
```html
<span class="tag tag-new">New</span>
<span class="tag tag-trending">Trending</span>
<span class="tag tag-primary">Popular</span>
```

### Grid Layouts
```html
<div class="grid grid-3">
    <!-- 3 columns on desktop, 2 on tablet, 1 on mobile -->
</div>
```

## How to View the Website

### Option 1: Direct File Opening
1. Navigate to the project folder
2. Double-click `index.html` to open it in your default web browser
3. All internal links will work correctly

### Option 2: Local Server (Recommended)
1. Open a terminal/command prompt in the project folder
2. For Python 3:
   ```bash
   python -m http.server 8000
   ```
3. For Python 2:
   ```bash
   python -m SimpleHTTPServer 8000
   ```
4. Open your browser and navigate to `http://localhost:8000`

### Option 3: VS Code Live Server
1. Install the "Live Server" extension in VS Code
2. Right-click on `index.html`
3. Select "Open with Live Server"

## Responsive Breakpoints

- **Mobile**: ≤ 480px
- **Tablet**: 481px - 1024px
- **Desktop**: > 1024px

## Browser Compatibility

The website is compatible with all modern browsers:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Features

### Navigation
- Sticky header that stays at the top while scrolling
- Responsive hamburger menu on mobile devices
- Smooth transitions and hover effects
- CSS-only implementation

### Pages

#### Home Page
- Hero section with gradient background and animations
- Introduction section
- Featured Courses section with tags and CTA
- Testimonials section with star ratings
- Enhanced footer with social links

#### Courses Page
- 5 course cards in responsive grid
- Each card includes title, description, and "View Course" button
- Hover effects with card lift animation

#### Blog Page
- 3 blog articles with tags (Trending, Popular, New)
- Enhanced card layout with header, body, and footer
- "Read More" buttons
- Responsive grid layout

#### About Page
- Vision section
- Mission section
- What We Offer section
- Card-based layout

#### Contact Page
- Contact form with validation
- Name, Email, Phone (optional), and Message fields
- HTML5 form validation
- Enhanced focus states

#### 404 Page
- Friendly error message
- Large 404 display
- "Go Back Home" button
- Consistent design

## CSS Architecture

### CSS Variables
All design tokens are defined as CSS variables in `:root`:
- Colors (primary, secondary, accent)
- Typography (h1-h4, p, small, line-heights)
- Spacing (xs, sm, md, lg, xl, xxl)
- Border radius
- Shadows
- Transitions

### Component Library
Separate `components.css` file containing:
- Button components (primary, secondary)
- Card components
- Badge/Tag components
- Grid layouts
- Social icons
- Testimonial cards
- Scroll-to-top button

### Animation System
- Keyframe animations defined in main CSS
- Utility classes for applying animations
- Smooth, performant animations using CSS transforms

## Accessibility Features

1. **Semantic HTML**: Proper use of HTML5 semantic elements
2. **ARIA Labels**: Screen reader support for all interactive elements
3. **Skip Link**: Keyboard navigation support
4. **Focus Indicators**: Visible focus states for all interactive elements
5. **Color Contrast**: High contrast ratios for readability
6. **Form Labels**: All form inputs have associated labels
7. **Heading Hierarchy**: Proper H1-H3 structure
8. **Alt Text Ready**: Structure in place for images with lazy loading

## Performance

- No JavaScript dependencies
- Pure CSS animations (hardware accelerated)
- Optimized CSS with component separation
- Fast page load times
- Lazy loading structure ready for images
- Efficient CSS selectors

## Design System

The website now includes a comprehensive design system:

### Color Palette
- Primary: #0066ff
- Background: #f4f6f8
- Text: #222222, #666666, #999999
- Cards: #ffffff

### Typography Scale
- H1: 2-2.5rem (responsive)
- H2: 1.6-2rem (responsive)
- H3: 1.25-1.5rem (responsive)
- Body: 0.9-1rem (responsive)

### Spacing System
- xs: 0.5rem
- sm: 1rem
- md: 1.5rem
- lg: 2rem
- xl: 3rem
- xxl: 4rem

## Screenshots

To capture screenshots of the responsive views:

1. **Desktop View**: Open browser at > 1024px width
2. **Tablet View**: Resize browser to 768px width
3. **Mobile View**: Resize browser to 375px width or use browser DevTools

### Recommended Screenshots:
- Home page (desktop, tablet, mobile)
- Featured Courses section
- Testimonials section
- Footer with social links
- 404 page
- Blog page with enhanced layout
- Mobile navigation menu

## Notes

- All forms are UI-only and do not submit data (as per requirements)
- External links point to enginow.in and social media platforms
- No JavaScript is used - all functionality is CSS-only
- The website is fully static and can be hosted on any static hosting service
- Images can be added with `loading="lazy"` attribute for performance
- All animations are CSS-only and hardware accelerated

## License

© 2024 Enginow. All rights reserved.
