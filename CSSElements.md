# CSS Properties Reference

## Table of Contents
- [Text Properties](#text-properties)
- [Box Model](#box-model)
- [Layout Properties](#layout-properties)
- [Background Properties](#background-properties)
- [Flexbox Properties](#flexbox-properties)
- [Grid Properties](#grid-properties)
- [Transform Properties](#transform-properties)
- [Transition & Animation](#transition--animation)
- [Media Queries](#media-queries)
- [Units & Selectors](#units--selectors)

## Text Properties
```css
/* Font and Text Styling */
.text-example {
    color: #333333;              /* Text color */
    font-family: Arial, sans-serif; /* Text font */
    font-size: 16px;            /* Text size */
    font-weight: bold;          /* Text thickness (100-900) */
}

/* Additional Text Properties */
.more-text {
    text-align: center;         /* Text alignment */
    line-height: 1.5;           /* Line spacing */
    text-decoration: underline; /* Text decoration */
    text-transform: uppercase;  /* Text case */
}
```

## Box Model
```css
/* Box Model Example */
.box-model {
    margin: 10px 20px;          /* Outside spacing */
    padding: 15px;              /* Inside spacing */
    border: 1px solid black;    /* Element border */
    border-radius: 5px;         /* Rounded corners */
}

/* Box Sizing */
.container {
    box-sizing: border-box;     /* Include padding in width */
    width: 100%;
    max-width: 1200px;
}
```

## Layout Properties
```css
/* Basic Layout */
.layout {
    display: block;             /* Element rendering type */
    position: relative;         /* Element positioning */
    width: 100%;               /* Element width */
    height: 300px;             /* Element height */
}

/* Positioning */
.positioned {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;                /* Stack order */
}
```

## Background Properties
```css
/* Background Styling */
.background {
    background-color: #ffffff;  /* Solid color */
    background-image: url('image.jpg'); /* Image */
    background-size: cover;     /* Image sizing */
    background-position: center;/* Image position */
    background-repeat: no-repeat; /* Image repetition */
}

/* Gradient Background */
.gradient {
    background: linear-gradient(to right, #ff0000, #00ff00);
}
```

## Flexbox Properties
```css
/* Flex Container */
.flex-container {
    display: flex;
    flex-direction: row;        /* Main axis direction */
    justify-content: center;    /* Main axis alignment */
    align-items: center;        /* Cross axis alignment */
    flex-wrap: wrap;           /* Allow wrapping */
}

/* Flex Items */
.flex-item {
    flex: 1;                   /* Grow and shrink */
    flex-basis: 200px;         /* Base width */
    align-self: stretch;       /* Individual alignment */
}
```

## Grid Properties
```css
/* Grid Container */
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Column layout */
    grid-template-rows: 100px auto;        /* Row layout */
    gap: 20px;                            /* Grid spacing */
}

/* Grid Items */
.grid-item {
    grid-column: span 2;       /* Column span */
    grid-row: 1 / 3;          /* Row positioning */
}
```

## Transform Properties
```css
/* Basic Transforms */
.transform {
    transform: rotate(45deg);              /* Rotation */
    transform: scale(1.5);                 /* Scaling */
    transform: translate(100px, 50px);     /* Movement */
    transform: skew(10deg);                /* Skewing */
}

/* Multiple Transforms */
.combined-transform {
    transform: rotate(45deg) scale(1.5);
}
```

## Transition & Animation
```css
/* Transitions */
.transition {
    transition: all 0.3s ease;  /* Property animation */
    opacity: 0.8;               /* Transparency */
}

/* Keyframe Animation */
@keyframes slide {
    from { transform: translateX(0); }
    to { transform: translateX(100px); }
}

.animated {
    animation: slide 2s infinite;
}
```

## Media Queries
```css
/* Responsive Design */
@media (max-width: 768px) {
    .responsive {
        flex-direction: column;
        width: 100%;
    }
}

@media (orientation: landscape) {
    .landscape {
        display: flex;
    }
}
```

## Units & Selectors
```css
/* Common Units */
.units {
    /* Absolute Units */
    width: 100px;              /* Pixels */
    margin: 1pt;               /* Points */
    
    /* Relative Units */
    width: 50%;                /* Percentage */
    font-size: 1.2em;          /* Relative to parent */
    padding: 2rem;             /* Relative to root */
    height: 100vh;             /* Viewport height */
    width: 100vw;              /* Viewport width */
}

/* Selectors */
.class-name { }                /* Class selector */
#id-name { }                   /* ID selector */
div { }                        /* Element selector */
div p { }                      /* Descendant selector */
div > p { }                    /* Child selector */
div + p { }                    /* Adjacent selector */
div, p { }                     /* Multiple selector */
```


