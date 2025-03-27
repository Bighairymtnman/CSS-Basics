# Advanced CSS Reference

## Complex Layouts
/* Grid Areas provide a powerful way to create complex page layouts using a visual ASCII representation.
   This makes it easier to understand and maintain layout structure. Grid areas are perfect for 
   creating responsive, full-page layouts with clear content organization. */

1. Grid Areas Layout
```css
.page-layout {
    display: grid;
    grid-template-areas:
        "header header header"
        "nav main sidebar"
        "footer footer footer";
    grid-template-columns: 200px 1fr 200px;
    gap: 20px;
}

.header { grid-area: header; }
.nav { grid-area: nav; }
.main { grid-area: main; }
.sidebar { grid-area: sidebar; }
.footer { grid-area: footer; }
```

## Advanced Animations
/* Modern CSS animations allow complex motion design without JavaScript.
   These techniques combine transforms, opacity, and timing functions to create
   smooth, engaging user experiences. Use these for interactive elements and 
   state changes. */

1. Custom Animation
```css
@keyframes slide-fade {
    0% {
        transform: translateX(-100px);
        opacity: 0;
    }
    50% {
        transform: translateX(10px);
        opacity: 0.5;
    }
    100% {
        transform: translateX(0);
        opacity: 1;
    }
}

.animated-element {
    animation: slide-fade 0.8s ease-out forwards;
}
```

2. Transform Combinations
/* Combining multiple transforms creates sophisticated hover effects.
   These effects add depth and interactivity to cards and clickable elements. */
```css
.card-hover {
    transition: all 0.3s ease;
}

.card-hover:hover {
    transform: translateY(-10px) rotate(2deg) scale(1.02);
    box-shadow: 0 15px 30px rgba(0,0,0,0.2);
}
```

## Advanced Flexbox
/* Flexbox can create complex layouts beyond simple row/column arrangements.
   This masonry-like layout uses flex-flow for a Pinterest-style grid,
   while maintaining flexibility and responsiveness. */

1. Masonry-like Layout
```css
.flex-masonry {
    display: flex;
    flex-flow: column wrap;
    max-height: 1000px;
    gap: 20px;
}

.flex-item {
    flex: 0 0 auto;
    width: calc(33.333% - 20px);
}
```

2. Custom Properties (CSS Variables)
/* CSS Variables enable dynamic, maintainable theming and responsive designs.
   They can be updated via JavaScript and respond to media queries, making
   them perfect for dark mode and dynamic theming. */
```css
:root {
    --primary-color: #2196f3;
    --spacing-unit: 8px;
    --max-width: 1200px;
}

.dynamic-theme {
    --text-color: var(--primary-color);
    --padding: calc(var(--spacing-unit) * 2);
    
    color: var(--text-color);
    padding: var(--padding);
    max-width: var(--max-width);
}

@media (prefers-color-scheme: dark) {
    :root {
        --primary-color: #90caf9;
    }
}
```

## Advanced Selectors
/* Advanced selectors target elements based on specific attributes and states.
   These powerful selectors reduce the need for extra classes and create more
   maintainable code. */

1. Advanced Attribute Selectors
```css
/* Matches elements with "data-" attributes containing "user" */
[data-*="user"] {
    background: #f0f8ff;
}

/* Matches exact language codes */
[lang|="en"] {
    font-family: 'English-Font', sans-serif;
}

/* Matches elements whose src ends with specific extensions */
img[src$=".svg"] {
    filter: drop-shadow(0 0 3px rgba(0,0,0,0.2));
}
```

2. Complex Pseudo-Elements
/* Pseudo-elements create decorative content without extra HTML.
   Perfect for quotes, borders, and visual enhancements. */
```css
.fancy-quote::before {
    content: '"';
    font-size: 4em;
    position: absolute;
    left: -0.5em;
    top: -0.2em;
    opacity: 0.1;
}

.gradient-border::after {
    content: '';
    position: absolute;
    inset: -2px;
    background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
    z-index: -1;
    border-radius: inherit;
}
```

## Visual Effects
/* Modern CSS filters and blend modes create sophisticated visual effects
   without image editing software. These effects can enhance images and
   create dynamic UI elements. */

1. Complex Filters
```css
.image-effects {
    filter: brightness(1.2) contrast(110%) saturate(1.2) hue-rotate(15deg);
}

.blur-backdrop {
    backdrop-filter: blur(8px) brightness(0.8);
    background-color: rgba(255, 255, 255, 0.1);
}

.duotone {
    filter: grayscale(100%) sepia(50%) hue-rotate(170deg);
}
```

2. Blend Modes
/* Blend modes combine layers of colors and images for creative effects.
   Use these for hero sections, overlays, and artistic elements. */
```css
.blend-overlay {
    background-blend-mode: overlay;
    background-image: 
        linear-gradient(45deg, #12c2e9, #c471ed),
        url('texture.jpg');
}

.text-blend {
    mix-blend-mode: difference;
    background: white;
    color: black;
}
```

## Advanced Responsive Design
/* Container queries and modern responsive techniques allow components to
   respond to their container size rather than just viewport size. This
   enables truly modular, responsive components. */

1. Container Queries
```css
@container (min-width: 400px) {
    .card {
        display: grid;
        grid-template-columns: 2fr 1fr;
    }
}

.card-container {
    container-type: inline-size;
    container-name: card;
}
```

2. Clamp and Fluid Typography
/* Fluid typography and spacing create smooth scaling across viewports.
   Perfect for responsive text and maintaining visual hierarchy. */
```css
.fluid-text {
    /* min: 16px, preferred: 3vw, max: 24px */
    font-size: clamp(1rem, 3vw, 1.5rem);
}

.fluid-spacing {
    /* Fluid padding that scales with viewport */
    padding: clamp(1rem, 5vw, 3rem);
    margin: clamp(1rem, calc(1rem + 2vw), 4rem);
}
```

## Dynamic CSS
/* Advanced CSS variables and calculations create dynamic, maintainable
   systems for spacing, colors, and layouts. These techniques power
   modern design systems and theming. */

1. Complex Custom Properties
```css
.theme-config {
    --base-size: 4;
    --spacing-unit: calc(var(--base-size) * 1px);
    --content-width: min(90vw, 1200px);
    --header-height: max(60px, 10vh);
    
    --primary-hue: 220;
    --primary-color: hsl(var(--primary-hue), 80%, 50%);
    --primary-light: hsl(var(--primary-hue), 80%, 80%);
    --primary-dark: hsl(var(--primary-hue), 80%, 20%);
}
```

2. Advanced Calculations
/* Complex calculations enable dynamic layouts that respond to both
   content and viewport. Perfect for app-like interfaces. */
```css
.dynamic-layout {
    --sidebar-width: 250px;
    --gap: 2rem;
    
    /* Calculate main content width */
    width: calc(100% - var(--sidebar-width) - var(--gap));
    
    /* Dynamic height calculations */
    height: calc(100vh - var(--header-height) - var(--footer-height));
    
    /* Complex calculations */
    padding: calc(var(--spacing-unit) * 2 + var(--gap));
}
```

## Performance Optimization
/* High-performance animations and loading states improve perceived
   performance and user experience. These techniques leverage GPU
   acceleration and efficient properties. */

1. GPU-Accelerated Animations
```css
.smooth-transform {
    will-change: transform;
    transform: translateZ(0);
    backface-visibility: hidden;
}

.efficient-animation {
    transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    animation-fill-mode: backwards;
}
```

2. Advanced Loading States
/* Skeleton screens provide better perceived performance than spinners.
   This creates a smooth loading animation for content placeholders. */
```css
.skeleton-loader {
    background: linear-gradient(
        90deg,
        rgba(190, 190, 190, 0.2) 25%,
        rgba(129, 129, 129, 0.24) 37%,
        rgba(190, 190, 190, 0.2) 63%
    );
    background-size: 400% 100%;
    animation: skeleton-loading 1.4s ease infinite;
}

@keyframes skeleton-loading {
    0% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0 50%;
    }
}
```



