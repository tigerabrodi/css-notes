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

## Box model

`box-sizing` is by default content-box. This means element's padding and border is included in the width calculation.

`border-box` is the value we want for all elements. Element's content is only what's included in the height or width.

## Padding

Pixel is the best unit for padding.

## Margin

A negative margin can pull an element outside its parent.

Negative margins can also pull an element's sibling closer. It's easy to fall into the trap of thinking that margin is exclusively about changing the selected element's position. Really, though, it's about changing the gap between elements. Negative margin shrinks the gap below an element, causing the next element to scoot up closer.

Auto margin used for centering within a container.

Sometimes you may want a wrapper element e.g. around an image and use negative margin to stretch the image.

## Flow layout

### Replaced elements

There's an exception to this rule: replaced elements.

A replaced element is one that embeds a "foreign" object. This includes:

```
<img />
<video />
<canvas />
```

Browser treats inline elements as typography, hence line-height is applied to those elements.

Inline-block elements internally act like block elements, but externally act like inline elements. The parent container will treat it as an inline element, since it's external. But the element itself can be styled like a block.

Here's the big downside with inline-block: It disables line-wrapping.

Fit-content will shrink down to the size of its content.

Fit-content behaves like max-content, though if the content is too wide to fit in the parent, it add line-breaks as-needed.

## Margin collapse

Only vertical margins collapse. Margin collapse is unique to Flow layout. Nesting elements doesn't prevent collapsing. Margins can collapse in the same direction. More than two margins can collapse.

Be aware of how you use margins. Don't set the specifically on components, in such cases it is better to use layout components. For reusable components, we want them to be as unopinionated as possible.

Margin is meant to increase the distance between siblings. It is not meant to increase the gap between a child and its parent's bounding box; that's what padding is for.

Margin will always try and increase distance between siblings, even if it means transferring margin to the parent element! In this case, the effect is the same as if we had applied the margin to the parent <div>, not the child <p>.

# Rendering logic 2

## Relative positioning

If an element is currently using Positioned layout and you want to opt out, you can set position to either static or initial.

## Absolute positioning

## Containing blocks

## Stacking context

A stacking context is a 3D space where HTML elements are stacked along the Z-axis (the axis coming out of the screen).

## Fixed positioning

## Overflow

## Sticky positioning

## Hidden content
