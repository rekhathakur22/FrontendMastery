# CSS `font-weight`

## Definition

The `font-weight` property controls **how thick or thin text appears**.
It is used to make text lighter, normal, bold, or extra bold depending
on the available font weights.

> **Definition:** `font-weight` specifies the weight (boldness) of the
> characters in a font.

------------------------------------------------------------------------

# Syntax

``` css
selector {
    font-weight: value;
}
```

Example:

``` css
h1 {
    font-weight: bold;
}

p {
    font-weight: 400;
}
```

------------------------------------------------------------------------

# Common Values

## Keyword Values

### `normal`

Equivalent to **400**.

``` css
p {
    font-weight: normal;
}
```

### `bold`

Equivalent to **700**.

``` css
h1 {
    font-weight: bold;
}
```

## Numeric Values

CSS supports numeric values from **100** to **900**.

    Value Description
  ------- ------------------
      100 Thin
      200 Extra Light
      300 Light
      400 Normal (Regular)
      500 Medium
      600 Semi Bold
      700 Bold
      800 Extra Bold
      900 Black (Heavy)

Example:

``` css
h1 { font-weight: 700; }
h2 { font-weight: 500; }
p  { font-weight: 300; }
```

> The browser can only use weights that actually exist in the font. If a
> font doesn't include `600`, the browser will choose the closest
> available weight.

------------------------------------------------------------------------

# How It Works

Imagine the following CSS:

``` css
h1 {
    font-weight: 700;
}
```

The browser:

1.  Checks which font is being used.
2.  Looks for the **700 (Bold)** version of that font.
3.  If unavailable, it picks the closest available weight.

------------------------------------------------------------------------

# Using Google Fonts

Example:

``` html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
```

``` css
body {
    font-family: "Poppins", sans-serif;
}

h1 {
    font-weight: 700;
}

p {
    font-weight: 400;
}
```

Only the requested weights (300, 400, 600, and 700) are downloaded.

------------------------------------------------------------------------

# Variable Fonts

Some modern fonts are **variable fonts**, allowing many weights from
**1--1000**.

Example:

``` css
h1 {
    font-weight: 650;
}
```

This works only if the font supports variable weights.

------------------------------------------------------------------------

# Inheritance

`font-weight` is an **inherited property**.

``` css
body {
    font-weight: 300;
}
```

All child elements inherit `300` unless they define another weight.

------------------------------------------------------------------------

# Best Practices

-   Use **400** for normal body text.
-   Use **600** or **700** for headings.
-   Load only the weights you need from Google Fonts.
-   Avoid using very light weights (`100`, `200`) for long paragraphs
    because they reduce readability.

------------------------------------------------------------------------

# Common Mistakes

## ❌ Assuming every font supports every weight

``` css
p {
    font-weight: 900;
}
```

If the font only has `400` and `700`, the browser will use the closest
available weight.

## ❌ Loading unnecessary weights

Don't download every weight if you only use two or three.

------------------------------------------------------------------------

# Interview Questions

### What does `font-weight` do?

It controls the thickness (boldness) of text.

### Is `bold` the same as `700`?

Yes. `bold` maps to **700**, while `normal` maps to **400**.

### Can every font use all weights from 100--900?

No. A font must provide those weights or be a variable font. Otherwise,
the browser selects the closest available weight.

### Is `font-weight` inherited?

Yes.

------------------------------------------------------------------------

# Quick Revision

  Property         Description
  ---------------- --------------------------------------
  `font-weight`    Controls text thickness
  Default value    `400` (`normal`)
  Bold value       `700` (`bold`)
  Range            `100–900`
  Inherited        ✅ Yes
  Variable fonts   Can support many intermediate values
