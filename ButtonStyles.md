# CSS Button Styles Guide

## Basic Buttons
/* Foundation button styles with states */

1. Standard Buttons
```css
.btn {
    display: inline-block;
    padding: 0.5rem 1rem;
    font-size: 1rem;
    font-weight: 500;
    line-height: 1.5;
    text-align: center;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
}

/* States */
.btn:hover {
    transform: translateY(-1px);
}

.btn:active {
    transform: translateY(1px);
}

.btn:disabled {
    opacity: 0.65;
    cursor: not-allowed;
}
```

## Button Variations
/* Common button style variations */

1. Filled Buttons
```css
.btn-primary {
    background: #007bff;
    color: white;
    border: none;
}

.btn-primary:hover {
    background: #0069d9;
}

.btn-success {
    background: #28a745;
    color: white;
    border: none;
}

.btn-danger {
    background: #dc3545;
    color: white;
    border: none;
}
```

2. Outline Buttons
```css
.btn-outline {
    background: transparent;
    border: 2px solid currentColor;
}

.btn-outline-primary {
    color: #007bff;
    border-color: #007bff;
}

.btn-outline-primary:hover {
    background: #007bff;
    color: white;
}
```

## Button Sizes
/* Size variations for different contexts */
```css
.btn-sm {
    padding: 0.25rem 0.5rem;
    font-size: 0.875rem;
}

.btn-lg {
    padding: 0.75rem 1.5rem;
    font-size: 1.25rem;
}

.btn-block {
    display: block;
    width: 100%;
}
```

## Icon Buttons
/* Buttons with icons and icon-only buttons */
```css
.btn-icon {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
}

.btn-icon-only {
    padding: 0.5rem;
    border-radius: 50%;
    aspect-ratio: 1;
}

/* Example with material icons */
.btn-icon i {
    font-size: 1.25em;
}
```

## Loading States
/* Button loading indicators */
```css
.btn-loading {
    position: relative;
    color: transparent !important;
}

.btn-loading::after {
    content: '';
    position: absolute;
    width: 1rem;
    height: 1rem;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border: 2px solid #ffffff;
    border-radius: 50%;
    border-right-color: transparent;
    animation: button-loading 0.75s linear infinite;
}

@keyframes button-loading {
    to {
        transform: translate(-50%, -50%) rotate(360deg);
    }
}
```

## Button Groups
/* Grouped button layouts */
```css
.btn-group {
    display: inline-flex;
    border-radius: 4px;
}

.btn-group .btn {
    border-radius: 0;
}

.btn-group .btn:first-child {
    border-top-left-radius: 4px;
    border-bottom-left-radius: 4px;
}

.btn-group .btn:last-child {
    border-top-right-radius: 4px;
    border-bottom-right-radius: 4px;
}
```

## Modern Button Effects
/* Contemporary button styles and animations */
```css
.btn-modern {
    background: linear-gradient(145deg, #007bff, #0056b3);
    border: none;
    color: white;
    box-shadow: 0 4px 15px rgba(0, 123, 255, 0.2);
}

.btn-modern:hover {
    box-shadow: 0 8px 25px rgba(0, 123, 255, 0.3);
}

.btn-glass {
    background: rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.1);
}

.btn-neon {
    border: 2px solid #007bff;
    box-shadow: 0 0 5px #007bff,
                0 0 25px #007bff;
}

.btn-neon:hover {
    box-shadow: 0 0 5px #007bff,
                0 0 25px #007bff,
                0 0 50px #007bff;
}
```

## Responsive Buttons
/* Mobile-friendly button adaptations */
```css
@media (max-width: 768px) {
    .btn {
        padding: 0.75rem 1rem;
    }
    
    .btn-block-mobile {
        display: block;
        width: 100%;
        margin-bottom: 0.5rem;
    }
    
    .btn-group {
        flex-direction: column;
    }
}
```
