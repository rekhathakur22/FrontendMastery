# CSS `text-align`

## Definition

The `text-align` property controls the **horizontal alignment of inline
content** (such as text, inline elements, and inline-block elements)
inside a block-level container.

> **Definition:** `text-align` specifies how inline content is
> horizontally aligned within its containing block.

------------------------------------------------------------------------

# Syntax

``` css
selector {
    text-align: value;
}
```

Example:

``` css
h1 {
    text-align: center;
}
```

------------------------------------------------------------------------

# Common Values

## `left`

Aligns text to the physical left side.

``` css
p {
    text-align: left;
}
```

------------------------------------------------------------------------

## `right`

Aligns text to the physical right side.

``` css
p {
    text-align: right;
}
```

------------------------------------------------------------------------

## `center`

Centers inline content horizontally.

``` css
h1 {
    text-align: center;
}
```

------------------------------------------------------------------------

## `justify`

Aligns text evenly along both left and right edges by adjusting word
spacing.

``` css
article p {
    text-align: justify;
}
```

------------------------------------------------------------------------

## `start`

Aligns text to the **start of the writing direction**.

-   LTR → Left
-   RTL → Right

``` css
p {
    text-align: start;
}
```

------------------------------------------------------------------------

## `end`

Aligns text to the **end of the writing direction**.

-   LTR → Right
-   RTL → Left

``` css
p {
    text-align: end;
}
```

------------------------------------------------------------------------

# `left` / `right` vs `start` / `end`

`left` and `right` are **physical directions**.

`start` and `end` are **logical directions** that depend on the
document's writing direction (`dir` attribute or `direction` property).

  Property   Type       LTR (English)   RTL (Arabic)
  ---------- ---------- --------------- --------------
  `left`     Physical   Left            Left
  `right`    Physical   Right           Right
  `start`    Logical    Left            Right
  `end`      Logical    Right           Left

Use **`start`** and **`end`** for multilingual websites.

------------------------------------------------------------------------

# Global Values

``` css
text-align: inherit;
text-align: initial;
text-align: unset;
text-align: revert;
```

-   `inherit` -- Uses the parent's computed value.
-   `initial` -- Resets to the initial value (`start`).
-   `unset` -- Behaves like `inherit` because `text-align` is inherited.
-   `revert` -- Restores the value from a lower-priority stylesheet.

------------------------------------------------------------------------

# Browser Rendering

When the browser processes:

``` css
text-align: center;
```

It:

1.  Calculates the container width.
2.  Measures the inline content.
3.  Computes the available horizontal space.
4.  Positions the content according to the selected alignment.

The element itself does **not** move.

------------------------------------------------------------------------

# `text-align` vs `margin: auto`

## `text-align`

Centers **inline content**.

``` css
h1 {
    text-align: center;
}
```

## `margin: auto`

Centers the **block element itself**.

``` css
.card {
    width: 300px;
    margin: 0 auto;
}
```

------------------------------------------------------------------------

# `text-align` vs `justify-content`

-   `text-align` aligns **text and inline content**.
-   `justify-content` aligns **Flexbox and Grid items**.

------------------------------------------------------------------------

# Inheritance

`text-align` is an **inherited property**.

``` css
body {
    text-align: center;
}
```

Child elements inherit the alignment unless overridden.

------------------------------------------------------------------------

# Real-World Examples

## Center Heading

``` css
h1 {
    text-align: center;
}
```

## Navigation

``` css
nav {
    text-align: center;
}
```

## Article

``` css
article p {
    text-align: justify;
}
```

## Price Column

``` css
.price {
    text-align: right;
}
```

------------------------------------------------------------------------

# Best Practices

-   Use `left` or `start` for body text.
-   Use `center` for headings.
-   Use `justify` carefully for long articles.
-   Prefer `start` and `end` for multilingual websites.

------------------------------------------------------------------------

# Common Mistakes

-   Trying to center a block element using `text-align`.
-   Center-aligning long paragraphs.
-   Confusing `text-align` with `justify-content`.

------------------------------------------------------------------------

# Accessibility

-   Left-aligned (`left`/`start`) text is generally easiest to read.
-   Center alignment is best for short text like headings.
-   Justified text can reduce readability in narrow columns.

------------------------------------------------------------------------

# Interview Questions

### What does `text-align` do?

It aligns inline content horizontally inside a block-level container.

### Does `text-align` move the element?

No. It only aligns the content inside the element.

### Is `text-align` inherited?

Yes.

### Difference between `left` and `start`?

-   `left` always means the physical left side.
-   `start` aligns to the beginning of the writing direction (LTR →
    left, RTL → right).

------------------------------------------------------------------------

# Quick Revision

  Value       Description
  ----------- ------------------------------------------
  `left`      Physical left alignment
  `right`     Physical right alignment
  `center`    Centers inline content
  `justify`   Aligns both edges
  `start`     Beginning of writing direction
  `end`       End of writing direction
  `inherit`   Uses parent's value
  `initial`   Resets to initial value
  `unset`     Behaves like `inherit`
  `revert`    Restores lower-priority stylesheet value

------------------------------------------------------------------------

# Complete Example

``` css
body {
    font-family: Arial, sans-serif;
}

h1 {
    text-align: center;
}

nav {
    text-align: center;
}

article p {
    text-align: justify;
}

.price {
    text-align: right;
}
```
