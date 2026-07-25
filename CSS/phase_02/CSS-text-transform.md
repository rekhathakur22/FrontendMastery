# CSS `text-transform`

## Definition

The `text-transform` property controls how the **capitalization of text
is displayed**. It changes the appearance of text without modifying the
original HTML content.

> **Definition:** `text-transform` specifies how text should be
> capitalized when rendered by the browser.

------------------------------------------------------------------------

# Syntax

``` css
selector {
    text-transform: value;
}
```

Example:

``` css
h1 {
    text-transform: uppercase;
}
```

------------------------------------------------------------------------

# Values

## `none` (Default)

No transformation is applied.

``` css
p {
    text-transform: none;
}
```

------------------------------------------------------------------------

## `uppercase`

Converts all letters to uppercase.

``` css
p {
    text-transform: uppercase;
}
```

Output:

``` text
FRONTEND MASTERY
```

------------------------------------------------------------------------

## `lowercase`

Converts all letters to lowercase.

``` css
p {
    text-transform: lowercase;
}
```

Output:

``` text
frontend mastery
```

------------------------------------------------------------------------

## `capitalize`

Capitalizes the first letter of each word.

``` css
p {
    text-transform: capitalize;
}
```

Output:

``` text
Frontend Mastery Css Notes
```

> Note: `capitalize` does not understand grammar or acronyms. For
> example, "css" becomes "Css", not "CSS".

------------------------------------------------------------------------

# Global Values

``` css
text-transform: inherit;
text-transform: initial;
text-transform: unset;
text-transform: revert;
```

-   **inherit** -- Uses the parent's computed value.
-   **initial** -- Resets to the specification-defined default (`none`).
-   **unset** -- Behaves like `inherit` for inherited properties,
    otherwise `initial`.
-   **revert** -- Restores the value from a lower-priority stylesheet
    (such as the browser stylesheet).

------------------------------------------------------------------------

# Browser Rendering

The browser:

1.  Reads the original text.
2.  Applies the requested transformation.
3.  Displays the transformed text.
4.  Leaves the HTML source unchanged.

Example:

HTML:

``` html
<p>Frontend Mastery</p>
```

CSS:

``` css
p {
    text-transform: uppercase;
}
```

Rendered Output:

``` text
FRONTEND MASTERY
```

The HTML remains unchanged.

------------------------------------------------------------------------

# Inheritance

`text-transform` is an **inherited property**.

``` css
body {
    text-transform: uppercase;
}
```

Child elements inherit `uppercase` unless overridden.

------------------------------------------------------------------------

# Common Use Cases

## Navigation

``` css
nav a {
    text-transform: uppercase;
}
```

## Buttons

``` css
button {
    text-transform: uppercase;
}
```

## Headings

``` css
h2 {
    text-transform: capitalize;
}
```

------------------------------------------------------------------------

# Best Practices

-   Use `uppercase` for buttons, navigation links, and labels.
-   Use `capitalize` carefully because it doesn't preserve acronyms.
-   Keep paragraph text as `none` for maximum readability.
-   Keep HTML content in its natural form and use CSS for presentation.

------------------------------------------------------------------------

# Common Mistakes

## Writing uppercase directly in HTML

❌

``` html
<h1>FRONTEND MASTERY</h1>
```

✅

``` html
<h1>Frontend Mastery</h1>
```

``` css
h1 {
    text-transform: uppercase;
}
```

------------------------------------------------------------------------

## Applying uppercase to long paragraphs

``` css
p {
    text-transform: uppercase;
}
```

Long uppercase text is generally harder to read.

------------------------------------------------------------------------

# Interview Questions

### What does `text-transform` do?

It changes the displayed capitalization of text without changing the
HTML.

### What is the default value?

`none`

### What is the difference between `uppercase` and `capitalize`?

-   `uppercase` converts every letter to uppercase.
-   `capitalize` converts only the first letter of each word to
    uppercase.

### Is `text-transform` inherited?

Yes.

### Does `text-transform` modify the HTML?

No. It only affects how text is rendered.

------------------------------------------------------------------------

# Quick Revision

  Value          Effect
  -------------- ----------------------------------------------
  `none`         No transformation
  `uppercase`    All letters uppercase
  `lowercase`    All letters lowercase
  `capitalize`   First letter of each word uppercase
  `inherit`      Copy parent's value
  `initial`      Reset to specification default (`none`)
  `unset`        `inherit` if inherited, otherwise `initial`
  `revert`       Restore value from lower-priority stylesheet

------------------------------------------------------------------------

# Example

``` css
body {
    font-family: "Inter", sans-serif;
}

h1 {
    text-transform: uppercase;
}

h2 {
    text-transform: capitalize;
}

button {
    text-transform: uppercase;
}

p {
    text-transform: none;
}
```
