# CSS `line-height`

## Definition

The `line-height` property controls the **height of each line of text**.
It determines the vertical spacing between lines, improving readability
and visual balance.

> **Definition:** `line-height` specifies the height of the line box
> used to render text.

------------------------------------------------------------------------

# Syntax

``` css
selector {
    line-height: value;
}
```

Example:

``` css
p {
    line-height: 1.5;
}
```

------------------------------------------------------------------------

# Why Use `line-height`?

-   Improves readability
-   Prevents text from looking cramped
-   Creates comfortable spacing for long paragraphs
-   Enhances accessibility

------------------------------------------------------------------------

# Common Values

## `normal`

Default browser value (typically around **1.2**, depending on the font).

``` css
p {
    line-height: normal;
}
```

## Unitless Number (Recommended)

``` css
p {
    line-height: 1.5;
}
```

Calculation:

    line-height = font-size × 1.5

If `font-size` is `20px`:

    20 × 1.5 = 30px

The line height automatically scales if the font size changes.

------------------------------------------------------------------------

## Pixels (`px`)

``` css
p {
    line-height: 30px;
}
```

The line height always remains `30px`.

------------------------------------------------------------------------

## Percentage

``` css
p {
    line-height: 150%;
}
```

Equivalent to `1.5` times the font size.

------------------------------------------------------------------------

## `em`

``` css
p {
    line-height: 1.8em;
}
```

Relative to the element's font size.

------------------------------------------------------------------------

# Unitless vs `px`

## Unitless (Preferred)

``` css
p {
    font-size: 20px;
    line-height: 1.5;
}
```

If the font size changes to `30px`, the computed line height becomes
`45px`.

## Fixed Pixels

``` css
p {
    font-size: 20px;
    line-height: 30px;
}
```

If the font size later changes to `30px`, the line height stays `30px`,
which may reduce readability.

------------------------------------------------------------------------

# Browser Rendering

The browser:

1.  Determines the font size.
2.  Calculates the line height.
3.  Creates a **line box** for each line.
4.  Centers the text vertically inside the line box.

The extra space is distributed above and below the text.

------------------------------------------------------------------------

# Inheritance

`line-height` is an **inherited property**.

``` css
body {
    line-height: 1.6;
}
```

Child elements inherit this value unless overridden.

------------------------------------------------------------------------

# Best Practices

-   Use **unitless values** whenever possible.
-   Use `1.5–1.6` for body text.
-   Use `1.1–1.3` for headings.
-   Avoid very small or very large line heights.
-   Test readability on desktop and mobile devices.

------------------------------------------------------------------------

# Common Mistakes

## Too Small

``` css
p {
    line-height: 0.8;
}
```

Lines may overlap.

## Too Large

``` css
p {
    line-height: 3;
}
```

Creates excessive spacing.

## Fixed Pixel Values Everywhere

``` css
p {
    line-height: 24px;
}
```

May not scale well when font sizes change.

------------------------------------------------------------------------

# Accessibility

A line height of **1.5** or greater for body text is commonly
recommended because it improves readability for many users, especially
when reading long-form content.

------------------------------------------------------------------------

# Interview Questions

### What does `line-height` do?

It controls the height of each line of text and the vertical spacing
between lines.

### Is `line-height` inherited?

Yes.

### Which value is recommended?

A unitless number such as `1.5`.

### What is the default value?

`normal`.

### What is the difference between `font-size` and `line-height`?

-   `font-size` controls the size of the characters.
-   `line-height` controls the height of the line box and spacing
    between lines.

------------------------------------------------------------------------

# Quick Revision

  Property        Description
  --------------- -------------------------------------------
  `line-height`   Controls line height and vertical spacing
  Default         `normal`
  Recommended     Unitless (`1.5`)
  Inherited       ✅ Yes
  Body Text       `1.5–1.6`
  Headings        `1.1–1.3`

------------------------------------------------------------------------

# Example

``` css
body {
    font-family: "Inter", sans-serif;
    font-size: 16px;
    line-height: 1.6;
}

h1 {
    font-size: 2.5rem;
    line-height: 1.2;
}

p {
    font-size: 1rem;
    line-height: 1.6;
}
```
