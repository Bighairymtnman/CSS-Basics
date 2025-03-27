# CSS Animations Reference Guide

## Basic Transitions
/* Smooth state changes for common interactions */

1. Property Transitions
```css
.smooth-transition {
    /* Single property */
    transition: opacity 0.3s ease;
    
    /* Multiple properties */
    transition: 
        transform 0.3s ease,
        opacity 0.2s ease-out,
        background-color 0.2s linear;
}

/* Common hover effects */
.hover-effect {
    transform: translateY(0);
    transition: transform 0.2s ease;
}

.hover-effect:hover {
    transform: translateY(-4px);
}
```

## Keyframe Animations
/* Reusable animation sequences */

1. Fade Animations
```css
@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes fadeOut {
    from {
        opacity: 1;
        transform: translateY(0);
    }
    to {
        opacity: 0;
        transform: translateY(20px);
    }
}

.fade-element {
    animation: fadeIn 0.5s ease forwards;
}
```

2. Attention Seekers
```css
@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.05); }
    100% { transform: scale(1); }
}

@keyframes shake {
    0%, 100% { transform: translateX(0); }
    25% { transform: translateX(-10px); }
    75% { transform: translateX(10px); }
}

.pulse { animation: pulse 1s infinite; }
.shake { animation: shake 0.5s ease-in-out; }
```

## Loading Animations
/* Common loading indicators */

1. Spinner
```css
@keyframes spin {
    to { transform: rotate(360deg); }
}

.spinner {
    width: 30px;
    height: 30px;
    border: 3px solid #f3f3f3;
    border-top: 3px solid #3498db;
    border-radius: 50%;
    animation: spin 1s linear infinite;
}
```

2. Pulse Loader
```css
@keyframes pulseLoader {
    0% { transform: scale(0); opacity: 1; }
    100% { transform: scale(1); opacity: 0; }
}

.pulse-loader {
    width: 20px;
    height: 20px;
    background: #3498db;
    border-radius: 50%;
    animation: pulseLoader 1s ease-out infinite;
}
```

## Page Transitions
/* Smooth transitions between states */

1. Page Entry/Exit
```css
.page-enter {
    opacity: 0;
    transform: translateX(-20px);
    animation: slideIn 0.3s ease forwards;
}

@keyframes slideIn {
    to {
        opacity: 1;
        transform: translateX(0);
    }
}

.page-exit {
    animation: slideOut 0.3s ease forwards;
}

@keyframes slideOut {
    to {
        opacity: 0;
        transform: translateX(20px);
    }
}
```

## Micro-interactions
/* Small, engaging animation details */

1. Button Feedback
```css
.button-interaction {
    transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}

.button-interaction:active {
    transform: scale(0.96);
}

.button-interaction.success {
    animation: successPop 0.4s ease;
}

@keyframes successPop {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}
```

## Advanced Effects
/* Complex animation combinations */

1. Parallax Scroll
```css
.parallax-container {
    perspective: 1px;
    height: 100vh;
    overflow-x: hidden;
    overflow-y: auto;
}

.parallax-layer {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    transform-origin: 0 0;
}

.parallax-back {
    transform: translateZ(-1px) scale(2);
}

.parallax-front {
    transform: translateZ(0);
}
```

2. Stagger Animation
```css
.stagger-item {
    opacity: 0;
    animation: fadeInUp 0.5s ease forwards;
}

.stagger-item:nth-child(1) { animation-delay: 0.1s; }
.stagger-item:nth-child(2) { animation-delay: 0.2s; }
.stagger-item:nth-child(3) { animation-delay: 0.3s; }

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
```

## Performance Tips
/* Optimizing animation performance */
```css
.performance-optimized {
    /* Use these properties for smooth animations */
    transform: translateZ(0);
    will-change: transform;
    backface-visibility: hidden;
}

/* Reduce motion when preferred */
@media (prefers-reduced-motion: reduce) {
    * {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
        scroll-behavior: auto !important;
    }
}
```
