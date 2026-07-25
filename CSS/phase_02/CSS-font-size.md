# CSS `font-size`

## Definition

The `font-size` property specifies **the size of text**. It controls how
large or small the characters are displayed on the screen.

> **Definition:** `font-size` sets the size of the font used to render
> text.

------------------------------------------------------------------------

# Syntax

``` css
selector {
    font-size: value;
}
```

Example:

``` css
h1 {
    font-size: 36px;
}

p {
    font-size: 16px;
}
```

------------------------------------------------------------------------

# Common Units

## 1. `px` (Pixels)

An absolute unit. Most commonly used.

``` css
p {
    font-size: 16px;
}
```

## 2. `em`

Relative to the **font size of the parent element**.

``` css
.parent {
    font-size: 20px;
}

.child {
    font-size: 1.5em;
}
```

Result:

    1.5 × 20px = 30px

## 3. `rem`

Relative to the **root (`html`) font size**.

``` css
html {
    font-size: 16px;
}

h1 {
    font-size: 2rem;
}
```

Result:

    2 × 16px = 32px

`rem` is generally preferred for scalable, maintainable layouts.

## 4. `%`

Relative to the parent's font size.

``` css
p {
    font-size: 125%;
}
```

## 5. Viewport Units

Responsive sizing based on the viewport.

``` css
h1 {
    font-size: 5vw;
}
```

------------------------------------------------------------------------

# Keyword Values

``` css
font-size: small;
font-size: medium;
font-size: large;
font-size: x-large;
```

These are rarely used in modern development.

------------------------------------------------------------------------

# Default Browser Font Size

Most browsers use:

``` css
16px
```

as the default body text size.

------------------------------------------------------------------------

# Inheritance

`font-size` is an **inherited property**.

``` css
body {
    font-size: 18px;
}
```

Child elements inherit `18px` unless overridden.

------------------------------------------------------------------------

# `em` vs `rem`

  `em`                           `rem`
  ------------------------------ --------------------------------
  Relative to parent             Relative to root (`html`)
  Can compound through nesting   Consistent throughout the page
  Useful for component scaling   Best choice for most layouts

------------------------------------------------------------------------

# Responsive Example

``` css
html {
    font-size: 16px;
}

h1 {
    font-size: clamp(2rem, 5vw, 4rem);
}

p {
    font-size: 1rem;
}
```

`clamp()` creates text that grows with the viewport while staying within
minimum and maximum limits.

------------------------------------------------------------------------

# Best Practices

-   Use **16px (1rem)** as a comfortable body text size.
-   Prefer **rem** for most layouts.
-   Use **em** when a component should scale with its parent.
-   Avoid very small text (below 12px) for readability.
-   Test font sizes on mobile and desktop devices.

------------------------------------------------------------------------

# Common Mistakes

## ❌ Using only `px` everywhere

This reduces flexibility when users change the root font size.

## ❌ Confusing `em` with `rem`

Remember:

-   `em` → parent
-   `rem` → root (`html`)

## ❌ Tiny text

``` css
p {
    font-size: 9px;
}
```

This is difficult to read.

------------------------------------------------------------------------

# Interview Questions

### What does `font-size` do?

It controls the size of text.

### What is the default browser font size?

Usually **16px**.

### What is the difference between `em` and `rem`?

-   `em` is relative to the parent element.
-   `rem` is relative to the root (`html`) element.

### Which unit is recommended for scalable websites?

`rem`.

### Is `font-size` inherited?

Yes.

------------------------------------------------------------------------

# Quick Revision

  Property               Description
  ---------------------- ------------------------------
  `font-size`            Sets the text size
  Default browser size   `16px`
  Absolute unit          `px`
  Relative units         `em`, `rem`, `%`, `vw`, `vh`
  Recommended            `rem`
  Inherited              ✅ Yes
