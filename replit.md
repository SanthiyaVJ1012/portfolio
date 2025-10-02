# Santhiya J - Personal Portfolio Website

## Overview

This is a premium personal portfolio website for Santhiya J, a B.Sc. Computer Science (AI & DS) student. The website showcases education, mini projects, technical skills, certifications, achievements, and professional information. The portfolio is built as a single-page application (SPA) with smooth scrolling navigation, interactive particle effects, and a modern responsive design.

**Tech Stack:** Vanilla HTML, CSS, and JavaScript with particles.js library for visual effects.

**Target Audience:** Recruiters, academic institutions, and professional network connections.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Single-Page Application (SPA) Design**
- **Problem:** Need to present comprehensive portfolio information in an easily navigable, professional format
- **Solution:** Single HTML file with section-based navigation using anchor links and smooth scrolling
- **Rationale:** Simplifies deployment, improves loading performance, and provides seamless user experience without page reloads

**Component-Based Structure**
- Modular sections: Hero, Stats, Education, Projects, Skills, Certifications, Achievements
- Each section is self-contained with consistent styling patterns
- Navigation automatically highlights active section based on scroll position

### Styling and Theming

**CSS Custom Properties (Variables) System**
- **Problem:** Need to support both light and dark themes with consistent color schemes
- **Solution:** CSS custom properties defined in `:root` and `[data-theme="dark"]`
- **Features:**
  - Automatic dark mode detection via `prefers-color-scheme` media query
  - Manual theme toggle with localStorage persistence
  - Smooth transitions between theme changes (0.3s ease)
- **Rationale:** Provides accessible viewing options while maintaining design consistency across themes

**Responsive Design**
- Mobile-first approach with breakpoint-based adaptations
- Hamburger menu for mobile navigation (≤768px viewport width)
- Horizontal scroll-snap for certifications list on mobile devices
- **Rationale:** Ensures optimal viewing experience across all device sizes

### Interactive Features

**Particles.js Background Effect**
- **Problem:** Need to create visual interest and modern aesthetic in hero section
- **Solution:** particles.js library integration for animated particle background
- **Configuration:** 80 particles with density-based distribution (800px value area)
- **Rationale:** Creates engaging, professional visual without heavy performance impact

**Theme Toggle Mechanism**
- Dual-state toggle button (sun/moon icons)
- Theme preference stored in localStorage
- Fallback to system preference on first visit
- **Rationale:** Respects user preferences and provides consistent experience across sessions

**Mobile Navigation**
- Toggle-based hamburger menu for mobile devices
- Auto-close on navigation link click for improved UX
- Active state management for current section
- **Rationale:** Standard mobile navigation pattern that users are familiar with

### State Management

**Client-Side State**
- Theme preference: Managed via localStorage API
- Navigation state: Toggle classes for mobile menu open/close
- Active section: Determined by scroll position (implied from navigation structure)
- **Rationale:** Simple state needs don't require framework; vanilla JavaScript provides sufficient functionality

### Performance Optimizations

**Loading Strategy**
- Inline critical CSS in `<head>` for faster first paint (implied by structure)
- Smooth scroll behavior via CSS (`scroll-behavior: smooth`)
- Transition properties for theme changes to avoid jarring updates
- **Rationale:** Fast initial load and smooth interactions enhance user experience

**SEO and Accessibility**
- Schema.org structured data (Person schema) for rich search results
- Semantic HTML structure for screen reader compatibility
- ARIA labels on interactive elements (theme toggle, mobile menu)
- Meta descriptions and proper heading hierarchy
- **Rationale:** Improves discoverability and ensures portfolio is accessible to all users

## External Dependencies

### Third-Party Libraries

**particles.js**
- **Purpose:** Animated particle background effect in hero section
- **Integration:** Client-side JavaScript library loaded via CDN (implied)
- **Configuration:** Custom particle density, count, and animation parameters
- **Rationale:** Lightweight library that provides sophisticated visual effects without custom WebGL implementation

### Browser APIs

**localStorage API**
- **Purpose:** Persist user theme preference across sessions
- **Fallback:** Defaults to system preference if no saved theme exists

**matchMedia API**
- **Purpose:** Detect system color scheme preference (`prefers-color-scheme`)
- **Usage:** Initial theme determination on first visit

### Asset Requirements

**Images and Icons**
- Profile photo: `assets/profile.jpg` (placeholder reference)
- Favicon: `assets/favicon.png` (placeholder reference)
- Theme icons: Emoji-based (☀️ sun, 🌙 moon) - no external dependency

**Note:** Asset files are referenced but not included in current repository structure; implementation requires adding these files to an `assets/` directory.