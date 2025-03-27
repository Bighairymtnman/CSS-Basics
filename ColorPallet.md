# CSS Color Reference Guide

## Basic Color Theory
/* Understanding these color relationships helps create harmonious designs */

1. Primary Colors
```css
.primary-colors {
    --blue: #007bff;
    --red: #dc3545;
    --yellow: #ffc107;
}
```

2. Secondary Colors
```css
.secondary-colors {
    --purple: #6f42c1;
    --green: #28a745;
    --orange: #fd7e14;
}
```

## Neutral Palette
/* Essential grays for text, backgrounds, and borders */
```css
.neutral-scale {
    --white: #ffffff;
    --gray-100: #f8f9fa;
    --gray-200: #e9ecef;
    --gray-300: #dee2e6;
    --gray-400: #ced4da;
    --gray-500: #adb5bd;
    --gray-600: #6c757d;
    --gray-700: #495057;
    --gray-800: #343a40;
    --gray-900: #212529;
    --black: #000000;
}
```

## Semantic Colors
/* Standard colors for feedback and status */
```css
.semantic-colors {
    --success: #28a745;
    --info: #17a2b8;
    --warning: #ffc107;
    --danger: #dc3545;
    --light: #f8f9fa;
    --dark: #343a40;
}
```

## Color Variations
/* Light and dark variations for hover states and hierarchy */
```css
.color-variations {
    /* Blues */
    --blue-100: #cce5ff;
    --blue-200: #99caff;
    --blue-300: #66afff;
    --blue-400: #3394ff;
    --blue-500: #007bff;
    --blue-600: #0062cc;
    --blue-700: #004999;
    --blue-800: #003166;
    --blue-900: #001833;

    /* Greens */
    --green-100: #d4edda;
    --green-200: #a9dbb4;
    --green-300: #7ec98f;
    --green-400: #53b769;
    --green-500: #28a745;
    --green-600: #208537;
    --green-700: #186429;
    --green-800: #10421b;
    --green-900: #08210d;
}
```

## Modern UI Colors
/* Contemporary color schemes for modern interfaces */
```css
.modern-ui {
    /* Slate */
    --slate-50: #f8fafc;
    --slate-100: #f1f5f9;
    --slate-200: #e2e8f0;
    --slate-300: #cbd5e1;
    --slate-400: #94a3b8;
    --slate-500: #64748b;
    --slate-600: #475569;
    --slate-700: #334155;
    --slate-800: #1e293b;
    --slate-900: #0f172a;

    /* Cool Gray */
    --cool-gray-50: #f9fafb;
    --cool-gray-100: #f3f4f6;
    --cool-gray-200: #e5e7eb;
    --cool-gray-300: #d1d5db;
    --cool-gray-400: #9ca3af;
    --cool-gray-500: #6b7280;
    --cool-gray-600: #4b5563;
    --cool-gray-700: #374151;
    --cool-gray-800: #1f2937;
    --cool-gray-900: #111827;
}
```

## Color Accessibility
/* WCAG 2.1 compliant color combinations */
```css
.accessible-combinations {
    /* Light Background + Dark Text */
    --light-bg: #ffffff;
    --dark-text: #212529;  /* 14.5:1 contrast ratio */

    /* Dark Background + Light Text */
    --dark-bg: #212529;
    --light-text: #f8f9fa;  /* 14.5:1 contrast ratio */

    /* Accent Colors with Good Contrast */
    --accessible-blue: #0056b3;  /* 4.5:1 on white */
    --accessible-red: #c92432;   /* 4.5:1 on white */
    --accessible-green: #2d8a3e; /* 4.5:1 on white */
}
```

## Usage Examples
/* Common color implementation patterns */
```css
.color-examples {
    /* Text Colors */
    color: var(--gray-700);
    
    /* Background Colors */
    background-color: var(--gray-100);
    
    /* Border Colors */
    border: 1px solid var(--gray-300);
    
    /* Hover States */
    &:hover {
        background-color: var(--blue-100);
        border-color: var(--blue-300);
    }
}

/* Dark Mode Example */
@media (prefers-color-scheme: dark) {
    :root {
        --text-color: var(--gray-200);
        --bg-color: var(--gray-900);
        --border-color: var(--gray-700);
    }
}
```
