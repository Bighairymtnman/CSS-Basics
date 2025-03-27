# CSS Basics Reference
This guide demonstrates common CSS patterns and implementations using properties from CSSElements.md.

## Styling Fundamentals
/* These patterns establish core visual styles using fundamental CSS properties.
   They create consistent, readable text and well-structured containers. */

1. Text Styling
/* Essential text styling combining font, size, and spacing properties
   for optimal readability */
```css
.text-example {
    font-family: Arial, sans-serif;
    font-size: 16px;
    line-height: 1.5;
    color: #333;
    text-align: left;
}
```

2. Box Model Implementation
/* Standard container pattern using the box model properties.
   Creates centered, width-constrained containers with consistent spacing */
```css
.container {
    width: 80%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 4px;
}
```

## Layout Patterns
/* These patterns provide solutions for common layout needs using
   flexbox and basic positioning properties */

1. Centered Content Layout
/* Simple centered layout pattern for main content areas */
```css
.centered-layout {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}
```

2. Two-Column Layout
/* Flexible two-column layout using flexbox.
   Sidebar has fixed width while main content flexes */
```css
.two-column {
    display: flex;
    gap: 20px;
}

.sidebar {
    flex: 0 0 300px;
}

.main-content {
    flex: 1;
}
```

3. Card Layout
/* Standard card pattern for content containers.
   Combines spacing, borders, and shadows for depth */
```css
.card {
    background: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    padding: 20px;
    margin-bottom: 20px;
}

.card-image {
    width: 100%;
    height: auto;
    border-radius: 8px 8px 0 0;
}

.card-content {
    padding: 15px;
}
```

## Navigation Patterns
/* Essential navigation patterns using flexbox and positioning.
   These create accessible, responsive navigation structures */

1. Horizontal Navigation
/* Basic horizontal navigation using flexbox for alignment */
```css
.nav-horizontal {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
}

.nav-horizontal li {
    margin-right: 20px;
}

.nav-horizontal a {
    text-decoration: none;
    color: #333;
    padding: 10px;
}
```

2. Responsive Navigation
/* Mobile-friendly navigation that adapts to screen size */
```css
.nav-responsive {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
}

/* Mobile Navigation */
@media (max-width: 768px) {
    .nav-responsive {
        flex-direction: column;
    }
    
    .nav-menu {
        display: none;
        width: 100%;
    }

    .nav-menu.active {
        display: block;
    }
}
```

3. Dropdown Menu
/* Simple dropdown menu using positioning and hover states */
```css
.dropdown {
    position: relative;
}

.dropdown-content {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    background: white;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.dropdown:hover .dropdown-content {
    display: block;
}
```

## Form Elements
/* Consistent form styling patterns for inputs and buttons.
   Creates accessible, user-friendly form interfaces */

1. Basic Form Layout
/* Standard form element styling with focus states */
```css
.form-group {
    margin-bottom: 20px;
}

.form-label {
    display: block;
    margin-bottom: 5px;
    font-weight: 500;
}

.form-input {
    width: 100%;
    padding: 8px 12px;
    border: 1px solid #ddd;
    border-radius: 4px;
}

.form-input:focus {
    outline: none;
    border-color: #007bff;
    box-shadow: 0 0 0 2px rgba(0,123,255,0.25);
}
```

2. Button Styles
/* Common button variations using color and border properties */
```css
.button {
    display: inline-block;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-weight: 500;
}

.button-primary {
    background: #007bff;
    color: white;
}

.button-secondary {
    background: #6c757d;
    color: white;
}

.button-outline {
    background: transparent;
    border: 2px solid #007bff;
    color: #007bff;
}
```

## Responsive Media
/* Patterns for handling images and media across different screen sizes */

1. Responsive Images
/* Basic responsive image handling with aspect ratio preservation */
```css
.img-fluid {
    max-width: 100%;
    height: auto;
    display: block;
}

.img-cover {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
}
```

2. Image Grids
/* Responsive image grid using CSS Grid */
```css
.image-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}

.image-grid img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 8px;
}
```

3. Background Images
/* Responsive background image handling with mobile optimization */
```css
.hero-section {
    background-image: url('../images/hero.jpg');
    background-size: cover;
    background-position: center;
    min-height: 400px;
}

/* Responsive background handling */
@media (max-width: 768px) {
    .hero-section {
        min-height: 300px;
        background-image: url('../images/hero-mobile.jpg');
    }
}
```

## Utility Classes
/* Reusable utility classes for common styling needs.
   These create consistent spacing and display patterns */

1. Spacing Utilities
/* Common spacing helpers for margin and padding */
```css
.margin-bottom {
    margin-bottom: 20px;
}

.padding-all {
    padding: 20px;
}

.no-margin {
    margin: 0;
}

.gap-20 {
    gap: 20px;
}
```

2. Display Utilities
/* Helper classes for controlling element display properties */
```css
.d-flex {
    display: flex;
}

.d-grid {
    display: grid;
}

.d-none {
    display: none;
}

@media (max-width: 768px) {
    .d-mobile-none {
        display: none;
    }
}
```

3. Text Utilities
/* Common text formatting helpers */
```css
.text-center {
    text-align: center;
}

.text-bold {
    font-weight: 700;
}

.text-truncate {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
```





