# CSS Grid Reference Guide

## Basic Grid Layouts
/* Foundation grid patterns */

1. Simple Grid
```css
.basic-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.basic-grid-responsive {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}
```

2. Grid Areas
```css
.layout-grid {
    display: grid;
    grid-template-areas:
        "header header header"
        "sidebar main main"
        "footer footer footer";
    grid-template-columns: 200px 1fr 1fr;
    gap: 20px;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
```

## Advanced Grid Patterns
/* Complex grid implementations */

1. Masonry Grid
```css
.masonry-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    grid-auto-rows: 20px;
    grid-auto-flow: dense;
}

.masonry-item {
    grid-row-end: span var(--span);
}
```

2. Dashboard Grid
```css
.dashboard-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-auto-rows: minmax(100px, auto);
    gap: 15px;
}

.widget-large {
    grid-column: span 2;
    grid-row: span 2;
}

.widget-wide {
    grid-column: span 4;
}
```

## Grid Alignment
/* Alignment and positioning techniques */
```css
.alignment-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    
    /* Container alignment */
    justify-content: center;
    align-content: center;
    
    /* Item alignment */
    justify-items: start;
    align-items: center;
}

.grid-item {
    /* Individual item alignment */
    justify-self: center;
    align-self: end;
}
```

## Responsive Grid Patterns
/* Adaptive grid layouts */
```css
.responsive-grid {
    display: grid;
    gap: 20px;
    
    /* Mobile */
    grid-template-columns: 1fr;
    
    /* Tablet */
    @media (min-width: 768px) {
        grid-template-columns: repeat(2, 1fr);
    }
    
    /* Desktop */
    @media (min-width: 1024px) {
        grid-template-columns: repeat(4, 1fr);
    }
}
```

## Grid Components
/* Common UI patterns using grid */

1. Card Grid
```css
.card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.card {
    display: grid;
    grid-template-rows: 200px 1fr auto;
}

.card-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
```

2. Feature Grid
```css
.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 40px 20px;
    padding: 40px;
}

.feature-item {
    display: grid;
    grid-template-rows: auto auto 1fr;
    gap: 10px;
    text-align: center;
}
```

## Grid Utilities
/* Helper classes for grid layouts */
```css
.grid {
    display: grid;
    gap: var(--gap, 20px);
}

.cols-2 { grid-template-columns: repeat(2, 1fr); }
.cols-3 { grid-template-columns: repeat(3, 1fr); }
.cols-4 { grid-template-columns: repeat(4, 1fr); }

.span-2 { grid-column: span 2; }
.span-3 { grid-column: span 3; }
.span-full { grid-column: 1 / -1; }

.auto-fit {
    grid-template-columns: repeat(auto-fit, minmax(var(--min, 250px), 1fr));
}

.auto-fill {
    grid-template-columns: repeat(auto-fill, minmax(var(--min, 250px), 1fr));
}
```

## Advanced Grid Techniques
/* Complex grid implementations */
```css
.holy-grail {
    display: grid;
    grid-template: 
        "header header header" auto
        "nav main aside" 1fr
        "footer footer footer" auto
        / auto 1fr auto;
    min-height: 100vh;
}

.subgrid {
    display: grid;
    grid-column: 1 / -1;
    grid-row: auto;
    grid-template-columns: subgrid;
}

.grid-overlap {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    
    & > * {
        grid-column: 1 / -1;
        grid-row: 1 / -1;
    }
}
```
