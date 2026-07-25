# CSS Combinators

## What are CSS Combinators?

A **combinator** is a symbol used to **combine two or more selectors** and define the relationship between them.

> **Definition:** A CSS combinator specifies the relationship between selectors, allowing you to target elements based on their position or relationship in the HTML document.

For example, instead of selecting every `<p>` element, you can select only the paragraphs that are inside a `<div>`.

---

# Why do we need Combinators?

Consider the following HTML:

```html
<div>
    <p>Paragraph 1</p>

    <section>
        <p>Paragraph 2</p>
    </section>
</div>

<p>Paragraph 3</p>
```

If you write:

```css
p {
    color: blue;
}
```

All three paragraphs become blue.

But what if you only want the paragraphs inside the `<div>`?

That's where combinators help.

---

# Types of CSS Combinators

There are **four main combinators** in CSS.

| Combinator | Name | Relationship |
|------------|------|--------------|
| (space) | Descendant Selector | Any descendant |
| `>` | Child Selector | Direct child |
| `+` | Adjacent Sibling Selector | Immediate next sibling |
| `~` | General Sibling Selector | All following siblings |

---

# 1. Descendant Combinator (Space)

**Syntax**

```css
ancestor descendant {
}
```

Example:

```css
div p {
    color: blue;
}
```

This selects **all `<p>` elements inside a `<div>`**, no matter how deeply they are nested.

### HTML

```html
<div>
    <p>Paragraph 1</p>

    <section>
        <p>Paragraph 2</p>
    </section>
</div>

<p>Paragraph 3</p>
```

### Output

- ✅ Paragraph 1 → Selected
- ✅ Paragraph 2 → Selected
- ❌ Paragraph 3 → Not selected

### Tree Representation

```
div
├── p ✅
└── section
     └── p ✅
```

Both paragraphs are descendants of `<div>`.

---

# 2. Child Combinator (`>`)

The child combinator selects **only direct children**.

**Syntax**

```css
parent > child {
}
```

Example:

```css
div > p {
    color: red;
}
```

### HTML

```html
<div>
    <p>Paragraph 1</p>

    <section>
        <p>Paragraph 2</p>
    </section>
</div>
```

### Output

- ✅ Paragraph 1 → Selected
- ❌ Paragraph 2 → Not selected

### Tree Representation

```
div
├── p ✅
└── section
     └── p ❌
```

Only direct children are selected.

---

# Descendant vs Child

HTML

```html
<div>
    <p>One</p>

    <section>
        <p>Two</p>
    </section>
</div>
```

Descendant:

```css
div p
```

Selects:

- One ✅
- Two ✅

Child:

```css
div > p
```

Selects:

- One ✅
- Two ❌

---

# 3. Adjacent Sibling Combinator (`+`)

Selects the **immediately following sibling**.

**Syntax**

```css
element1 + element2 {
}
```

Example:

```css
h1 + p {
    color: green;
}
```

### HTML

```html
<h1>Heading</h1>

<p>Paragraph 1</p>

<p>Paragraph 2</p>
```

### Output

- ✅ Paragraph 1 → Selected
- ❌ Paragraph 2 → Not selected

Only the first paragraph immediately after `<h1>` is selected.

### Tree Representation

```
h1
p ✅
p ❌
```

---

# 4. General Sibling Combinator (`~`)

Selects **all following siblings**.

**Syntax**

```css
element1 ~ element2 {
}
```

Example:

```css
h1 ~ p {
    color: blue;
}
```

### HTML

```html
<h1>Heading</h1>

<p>Paragraph 1</p>

<p>Paragraph 2</p>

<p>Paragraph 3</p>
```

### Output

- ✅ Paragraph 1
- ✅ Paragraph 2
- ✅ Paragraph 3

All following sibling paragraphs are selected.

---

# Adjacent vs General Sibling

HTML

```html
<h1>Heading</h1>

<p>One</p>

<p>Two</p>

<p>Three</p>
```

Adjacent sibling:

```css
h1 + p
```

Output

```
One ✅
Two ❌
Three ❌
```

General sibling:

```css
h1 ~ p
```

Output

```
One ✅
Two ✅
Three ✅
```

---

# Visual Summary

```
<div>
    <p>One</p>

    <section>
        <p>Two</p>
    </section>
</div>

<p>Three</p>
```

### `div p`

```
One ✅
Two ✅
Three ❌
```

### `div > p`

```
One ✅
Two ❌
Three ❌
```

---

```
<h1>Heading</h1>

<p>One</p>

<p>Two</p>

<p>Three</p>
```

### `h1 + p`

```
One ✅
Two ❌
Three ❌
```

### `h1 ~ p`

```
One ✅
Two ✅
Three ✅
```

---

# Real-world Examples

### Navigation Menu

```css
nav a {
    text-decoration: none;
}
```

Selects all links inside `<nav>`.

---

### Direct List Items

```css
ul > li {
    list-style: none;
}
```

Selects only direct `<li>` children of `<ul>`.

---

### Error Message

```css
input + span {
    color: red;
}
```

Styles the `<span>` immediately after an input.

---

### All Messages After Heading

```css
h2 ~ p {
    margin-top: 10px;
}
```

Styles all paragraph siblings after the heading.

---

# Interview Questions

## 1. What is a CSS combinator?

A CSS combinator is a symbol that combines selectors to target elements based on their relationship in the HTML document.

---

## 2. How many combinators are there in CSS?

There are **four** main combinators:

- Descendant (` `)
- Child (`>`)
- Adjacent Sibling (`+`)
- General Sibling (`~`)

---

## 3. What is the difference between a descendant and a child combinator?

- **Descendant (` `)** selects all matching descendants, regardless of nesting level.
- **Child (`>`)** selects only direct children.

---

## 4. What is the difference between `+` and `~`?

- `+` selects only the **immediately following sibling**.
- `~` selects **all following siblings** that share the same parent.

---

# Quick Revision

| Combinator | Meaning |
|------------|---------|
| `A B` | Select all `B` elements inside `A` |
| `A > B` | Select direct child `B` of `A` |
| `A + B` | Select the first `B` immediately after `A` |
| `A ~ B` | Select all `B` siblings after `A` |

---

# Memory Trick

Think of the relationships like a family:

- **Space (` `)** → **Children, grandchildren, great-grandchildren...** (all descendants)
- **`>`** → **Only direct children**
- **`+`** → **Your immediate next sibling**
- **`~`** → **All younger siblings after you**