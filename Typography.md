# CSS Typography Reference Guide

## Font Fundamentals
/* Core typography settings */

1. Font Scale
```css
:root {
    --font-xs: 0.75rem;    /* 12px */
    --font-sm: 0.875rem;   /* 14px */
    --font-base: 1rem;     /* 16px */
    --font-lg: 1.125rem;   /* 18px */
    --font-xl: 1.25rem;    /* 20px */
    --font-2xl: 1.5rem;    /* 24px */
    --font-3xl: 1.875rem;  /* 30px */
    --font-4xl: 2.25rem;   /* 36px */
    --font-5xl: 3rem;      /* 48px */
}
```

2. Font Families
```css
:root {
    /* System Font Stack */
    --font-sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 
                 'Helvetica Neue', Arial, sans-serif;
    
    /* Serif Stack */
    --font-serif: Georgia, Cambria, 'Times New Roman', Times, serif;
    
    /* Monospace Stack */
    --font-mono: SFMono-Regular, Menlo, Monaco, Consolas, 
                'Liberation Mono', 'Courier New', monospace;
}
```

## Text Styles
/* Common text patterns */

1. Headings
```css
.heading-styles {
    h1 {
        font-size: var(--font-4xl);
        line-height: 1.2;
        margin-bottom: 1rem;
        font-weight: 700;
    }

    h2 {
        font-size: var(--font-3xl);
        line-height: 1.3;
        margin-bottom: 0.75rem;
    }

    h3 {
        font-size: var(--font-2xl);
        line-height: 1.4;
        margin-bottom: 0.5rem;
    }
}
```

2. Body Text
```css
.body-text {
    font-size: var(--font-base);
    line-height: 1.6;
    color: var(--text-primary);
}

.lead-text {
    font-size: var(--font-lg);
    line-height: 1.6;
    font-weight: 300;
}

.small-text {
    font-size: var(--font-sm);
    line-height: 1.5;
}
```

## Typography Utilities
/* Helper classes for text styling */
```css
.text-utils {
    .text-truncate {
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }

    .text-break {
        word-break: break-word;
        overflow-wrap: break-word;
    }

    .text-center { text-align: center; }
    .text-right { text-align: right; }
    .text-justify { text-align: justify; }

    .uppercase { text-transform: uppercase; }
    .capitalize { text-transform: capitalize; }
    
    .font-light { font-weight: 300; }
    .font-normal { font-weight: 400; }
    .font-medium { font-weight: 500; }
    .font-bold { font-weight: 700; }
}
```

## Responsive Typography
/* Fluid and responsive text scaling */
```css
.fluid-type {
    /* Fluid heading */
    --fluid-h1: clamp(2rem, 5vw + 1rem, 4rem);
    --fluid-h2: clamp(1.5rem, 3vw + 1rem, 3rem);
    
    /* Fluid body */
    --fluid-text: clamp(1rem, 1.5vw + 0.5rem, 1.25rem);
}

@media (max-width: 768px) {
    .responsive-text {
        --font-4xl: 2rem;
        --font-3xl: 1.75rem;
        --font-2xl: 1.5rem;
    }
}
```

## Article Typography
/* Blog and article text styling */
```css
.article {
    max-width: 65ch;
    margin: 0 auto;

    p {
        margin-bottom: 1.5em;
    }

    h2 {
        margin-top: 2em;
        margin-bottom: 1em;
    }

    ul, ol {
        margin-bottom: 1.5em;
        padding-left: 1.5em;
    }

    blockquote {
        font-style: italic;
        border-left: 4px solid currentColor;
        margin-left: 0;
        padding-left: 1.5em;
    }
}
```

## Special Text Effects
/* Advanced typography treatments */
```css
.text-effects {
    .gradient-text {
        background: linear-gradient(45deg, #12c2e9, #c471ed);
        -webkit-background-clip: text;
        color: transparent;
    }

    .text-shadow {
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
    }

    .outlined-text {
        -webkit-text-stroke: 2px currentColor;
        color: transparent;
    }
}
```

## Font Performance
/* Optimizing font loading */
```css
/* Font loading strategies */
@font-face {
    font-family: 'CustomFont';
    src: url('/fonts/CustomFont.woff2') format('woff2'),
         url('/fonts/CustomFont.woff') format('woff');
    font-display: swap;
    font-weight: 400;
    font-style: normal;
}

/* Font subsetting example */
.subset-latin {
    font-family: 'CustomFont';
    unicode-range: U+0000-00FF;
}
```
