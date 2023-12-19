# Fundamentals

## Color

Use HSL color. Easy to to understand, modify and work with.

`background-color: hsl(32deg 68% 50%)` -> (Hue/Saturation/Lightness)

`hsl(120deg 75% 25% / 0.6)` -> last part is the opacity here.

## Units

> Please note, you shouldn't actually set a px font size on the html tag. This will override a user's chosen default font size.

Use rems for typography due to the accessibility benefits. Users may higher their default browser font size.

## Typography

line-height takes a unitless number. This number is multiplied by the element's font-size to calculate the actual line height.

To comply with accessibility guidelines, our body text should have a minimum line-height of 1.5.

# Rendering logic 1
