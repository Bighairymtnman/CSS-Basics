# CSS Properties Reference

## Text Properties
- `color`: Text color
  - Values: color names, hex, rgb(), rgba()
  - Example: `color: #333333;`

- `font-family`: Text font
  - Values: font names, generic families
  - Example: `font-family: Arial, sans-serif;`

- `font-size`: Text size
  - Values: px, em, rem, %
  - Example: `font-size: 16px;`

- `font-weight`: Text thickness
  - Values: normal, bold, 100-900
  - Example: `font-weight: bold;`

## Box Model Properties
- `margin`: Outside spacing
  - Values: px, em, rem, %
  - Example: `margin: 10px 20px;`

- `padding`: Inside spacing
  - Values: px, em, rem, %
  - Example: `padding: 15px;`

- `border`: Element border
  - Values: width style color
  - Example: `border: 1px solid black;`



## Layout Properties
- `display`: Element rendering type
  - Values: block, inline, flex, grid, none
  - Example: `display: flex;`

- `position`: Element positioning
  - Values: static, relative, absolute, fixed
  - Example: `position: relative;`

- `width`: Element width
  - Values: px, em, rem, %, auto
  - Example: `width: 100%;`

- `height`: Element height
  - Values: px, em, rem, %, auto
  - Example: `height: 300px;`

## Background Properties
- `background-color`: Element background
  - Values: color names, hex, rgb(), rgba()
  - Example: `background-color: #ffffff;`

- `background-image`: Background image
  - Values: url(), gradients
  - Example: `background-image: url('image.jpg');`

- `background-size`: Image sizing
  - Values: cover, contain, px, %
  - Example: `background-size: cover;`






## Flexbox Properties
- `flex-direction`: Main axis direction
  - Values: row, column, row-reverse, column-reverse
  - Example: `flex-direction: row;`

- `justify-content`: Main axis alignment
  - Values: flex-start, center, flex-end, space-between, space-around
  - Example: `justify-content: center;`

- `align-items`: Cross axis alignment
  - Values: stretch, flex-start, center, flex-end
  - Example: `align-items: center;`

## Grid Properties
- `grid-template-columns`: Column layout
  - Values: px, fr, repeat(), auto
  - Example: `grid-template-columns: repeat(3, 1fr);`

- `grid-template-rows`: Row layout
  - Values: px, fr, repeat(), auto
  - Example: `grid-template-rows: 100px auto;`

- `gap`: Grid spacing
  - Values: px, em, rem
  - Example: `gap: 20px;`

## Transform Properties
- `transform`: Element transformation
  - Values: rotate(), scale(), translate(), skew()
  - Example: `transform: rotate(45deg);`





## Transition & Animation Properties
- `transition`: Property animation
  - Values: property duration timing-function delay
  - Example: `transition: all 0.3s ease;`

- `opacity`: Element transparency
  - Values: 0 to 1
  - Example: `opacity: 0.8;`

## Media Query Properties
- `@media`: Responsive breakpoints
  - Values: screen width, orientation
  - Example: `@media (max-width: 768px)`

## Common Units
- Absolute: px, pt
- Relative: %, em, rem, vh, vw
- Colors: name, #hex, rgb(), hsl()

## Selectors Quick Reference
- Class: `.classname`
- ID: `#idname`
- Element: `div`
- Nested: `div p`
- Multiple: `div, p`



