# CSS `text-decoration`

## Definition

The `text-decoration` property is used to **add, remove, or customize
decorative lines on text**, such as underlines, overlines, and
line-through effects.

> **Definition:** `text-decoration` is a shorthand property that
> controls the decoration **line**, **color**, **style**, and
> **thickness**.

------------------------------------------------------------------------

# Syntax

``` css
selector {
    text-decoration: value;
}
```

Example:

``` css
p {
    text-decoration: underline;
}
```

------------------------------------------------------------------------

# Shorthand Property

The declaration:

``` css
text-decoration: underline;
```

is equivalent to:

``` css
text-decoration-line: underline;
text-decoration-color: currentColor;
text-decoration-style: solid;
text-decoration-thickness: auto;
```

------------------------------------------------------------------------

# `text-decoration-line`

## `none`

Removes any decoration.

``` css
a {
    text-decoration: none;
}
```

## `underline`

Draws a line below the text.

``` css
p {
    text-decoration: underline;
}
```

## `overline`

Draws a line above the text.

``` css
p {
    text-decoration: overline;
}
```

## `line-through`

Draws a line through the center of the text.

``` css
.completed {
    text-decoration: line-through;
}
```

Common uses:

-   Completed tasks
-   Old prices
-   Deleted content

## Multiple Lines

``` css
p {
    text-decoration: underline overline;
}
```

------------------------------------------------------------------------

# `text-decoration-color`

Changes only the decoration line color.

``` css
p {
    text-decoration: underline;
    text-decoration-color: red;
}
```

------------------------------------------------------------------------

# `text-decoration-style`

Controls the appearance of the decoration line.

``` css
text-decoration-style: solid;
text-decoration-style: dashed;
text-decoration-style: dotted;
text-decoration-style: double;
text-decoration-style: wavy;
```

------------------------------------------------------------------------

# `text-decoration-thickness`

Controls the thickness of the decoration.

``` css
p {
    text-decoration: underline;
    text-decoration-thickness: 3px;
}
```

------------------------------------------------------------------------

# Complete Example

``` css
p {
    text-decoration-line: underline;
    text-decoration-style: dashed;
    text-decoration-color: blue;
    text-decoration-thickness: 3px;
}
```

Shorthand:

``` css
p {
    text-decoration: underline dashed blue 3px;
}
```

------------------------------------------------------------------------

# Browser Rendering

The browser:

1.  Draws the text.
2.  Calculates the decoration position.
3.  Draws the decoration line.
4.  Applies the selected color.
5.  Applies the selected style.
6.  Applies the selected thickness.

------------------------------------------------------------------------

# Default Link Decoration

Browsers typically underline hyperlinks.

``` css
a {
    text-decoration: underline;
}
```

To remove it:

``` css
a {
    text-decoration: none;
}
```

------------------------------------------------------------------------

# Real-World Examples

## Navigation

``` css
nav a {
    text-decoration: none;
}
```

## Hover Effect

``` css
a:hover {
    text-decoration: underline;
}
```

## Completed Task

``` css
.completed {
    text-decoration: line-through;
}
```

## Discount Price

``` css
.old-price {
    text-decoration: line-through;
}
```

------------------------------------------------------------------------

# `text-decoration` vs `border-bottom`

## `text-decoration`

-   Designed for text decoration
-   Follows the text
-   Wraps correctly across multiple lines

## `border-bottom`

-   Draws a border around the element
-   Not a true underline
-   Positioned differently from text

------------------------------------------------------------------------

# Inheritance

`text-decoration` itself is **not inherited** like `color` or
`font-family`.

However, a decoration (such as an underline) can visually continue
across descendant text because the browser paints the decoration across
the text flow.

------------------------------------------------------------------------

# Best Practices

-   Use `text-decoration` for true underlines.
-   Remove underlines from links only if another clear visual cue
    exists.
-   Use `line-through` for completed items or old prices.
-   Avoid underlining long paragraphs.

------------------------------------------------------------------------

# Common Mistakes

## Removing all link underlines

``` css
a {
    text-decoration: none;
}
```

Always provide another indicator that links are clickable.

## Using `border-bottom` instead of `text-decoration`

``` css
border-bottom: 1px solid black;
```

This is not a true text underline.

------------------------------------------------------------------------

# Accessibility

Underlines clearly communicate that text is clickable.

If you remove them, use another indicator such as:

-   Color contrast
-   Hover effects
-   Icons
-   Background changes

------------------------------------------------------------------------

# Interview Questions

## What does `text-decoration` do?

It adds, removes, or customizes decorative lines on text.

## Is `text-decoration` a shorthand property?

Yes. It controls:

-   `text-decoration-line`
-   `text-decoration-color`
-   `text-decoration-style`
-   `text-decoration-thickness`

## How do you remove an underline from a link?

``` css
a {
    text-decoration: none;
}
```

## What is `line-through` used for?

-   Completed tasks
-   Old prices
-   Deleted content

## Difference between `text-decoration` and `border-bottom`?

-   `text-decoration` creates a true text decoration.
-   `border-bottom` draws a border around the element.

------------------------------------------------------------------------

# Quick Revision

  Property / Value              Description
  ----------------------------- ---------------------------
  `none`                        Removes decoration
  `underline`                   Draws a line below text
  `overline`                    Draws a line above text
  `line-through`                Draws a line through text
  `text-decoration-color`       Sets decoration color
  `text-decoration-style`       Sets line style
  `text-decoration-thickness`   Sets line thickness

------------------------------------------------------------------------

# Final Example

``` css
a {
    text-decoration: underline dashed blue 2px;
}

button {
    text-decoration: none;
}

.completed {
    text-decoration: line-through;
}
```
