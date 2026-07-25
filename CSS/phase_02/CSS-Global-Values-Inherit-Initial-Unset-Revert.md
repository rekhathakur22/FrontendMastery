# CSS Global Values for `text-transform`

Although the examples below use `text-transform`, these **CSS Global
Values** work with almost every CSS property.

------------------------------------------------------------------------

# 1. `inherit`

## Definition

`inherit` tells an element to **use the computed value from its parent
element**.

Think of it as:

> "Use the same value as my parent."

### Example

``` html
<div>
  <p>Hello CSS</p>
</div>
```

``` css
div {
    text-transform: uppercase;
}

p {
    text-transform: inherit;
}
```

### Output

``` text
HELLO CSS
```

The `<p>` inherits `uppercase` from its parent.

### When to Use

Useful when you want child elements to always match the parent's
styling.

------------------------------------------------------------------------

# 2. `initial`

## Definition

`initial` resets a property to its **initial value defined by the CSS
specification**, ignoring the parent's value.

For `text-transform`, the initial value is:

``` css
none
```

### Example

``` css
body {
    text-transform: uppercase;
}

p {
    text-transform: initial;
}
```

### Output

``` text
Hello CSS
```

Even though the parent is uppercase, the paragraph uses the property's
default (`none`).

------------------------------------------------------------------------

# 3. `unset`

## Definition

`unset` behaves differently depending on whether the property is
inherited.

-   If the property **is inherited** → `unset` behaves like `inherit`.
-   If the property **is not inherited** → `unset` behaves like
    `initial`.

Since `text-transform` is inherited:

``` css
body {
    text-transform: uppercase;
}

p {
    text-transform: unset;
}
```

### Output

``` text
HELLO CSS
```

For a non-inherited property such as `margin`:

``` css
div {
    margin: 50px;
}

p {
    margin: unset;
}
```

The computed margin becomes the initial value (`0`).

### Easy Rule

``` text
Inherited property?
        │
      Yes ──► unset = inherit
        │
       No ──► unset = initial
```

------------------------------------------------------------------------

# 4. `revert`

## Definition

`revert` removes the current declaration and restores the value that
would have come from a **lower-priority stylesheet**, such as the
browser's default stylesheet.

### Example

Browser stylesheet:

``` css
h1 {
    text-transform: none;
}
```

Your stylesheet:

``` css
h1 {
    text-transform: uppercase;
}

h1.special {
    text-transform: revert;
}
```

### Output

``` text
Hello CSS
```

`revert` restores the browser stylesheet value instead of using the
current rule.

------------------------------------------------------------------------

# `initial` vs `revert`

  -----------------------------------------------------------------------
  `initial`                              `revert`
  -------------------------------------- --------------------------------
  Uses the property's                    Restores the value from a
  specification-defined default value    lower-priority stylesheet

  Ignores parent and browser stylesheet  Returns to browser/user/default
                                         stylesheet behavior
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Visual Summary

``` text
Parent
│
├── inherit
│      ↓
│   Parent's value
│
├── initial
│      ↓
│   CSS specification default
│
├── unset
│      ↓
│   Inherited? → inherit
│   Not inherited? → initial
│
└── revert
       ↓
Previous stylesheet
(browser or user stylesheet)
```

------------------------------------------------------------------------

# Comparison Table

  -------------------------------------------------------------------------
  Keyword        Meaning          `text-transform` Result
  -------------- ---------------- -----------------------------------------
  `inherit`      Copy the         Parent's value
                 parent's value   

  `initial`      Reset to         `none`
                 specification    
                 default          

  `unset`        `inherit` if     Parent's value
                 inherited,       
                 otherwise        
                 `initial`        

  `revert`       Restore value    Browser/user stylesheet value
                 from             
                 lower-priority   
                 stylesheet       
  -------------------------------------------------------------------------

------------------------------------------------------------------------

# Interview Questions

## What is the difference between `inherit` and `initial`?

-   `inherit` copies the parent's computed value.
-   `initial` resets to the property's specification-defined default.

## When does `unset` behave like `inherit`?

When the property is inherited, such as `text-transform`, `color`, and
`font-family`.

## What is the difference between `initial` and `revert`?

-   `initial` uses the specification-defined default.
-   `revert` restores the value from a lower-priority stylesheet.

------------------------------------------------------------------------

# Memory Trick

``` text
inherit → Copy Parent

initial → Factory Default

unset → Smart Choice
          (inherit or initial)

revert → Go Back
          (previous stylesheet)
```
