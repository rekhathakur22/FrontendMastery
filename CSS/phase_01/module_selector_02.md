# What is CSS selector ?
CSS selectors are the pattern used to target the html element for styling.

# Type of CSS selector
- Universal Selector(*) 

# Universal Selector(*)
- select every element on the page
- apply mentioned style on page 
- used to reset css 
```css
*{
    property: value;
}
```
# Element(type) selector ?
- select all element of specified type and apply style to all of them 
```css
p{
  text:green;
}
```

# class selector(.)
- select elements of specific class name 
```css
.className{
  text:gree;
}
```

# id selector (#)
id selector select one element of particular id
```css
#id_name{
  text:green;
}
```
# Grouping Selector (,)
- select multiple element element of diffrent type and apply style to them
```css
h1,h2,p{
  text:green;
}
```

# 6. Descendant Selector (space)

Selects elements inside another element, at any depth.

```css
div p {
    color: blue;
}
```

```HTML

<div>
    <section>
        <p>Hello</p>
    </section>
</div>


<p>Outside</p>
```

Only the <p> inside <div> is selected.

# 7. Child Selector (>)

Selects only direct children.

```css
div > p {
    color: red;
}
```
```HTML

<div>
    <p>Direct Child</p>

    <section>
        <p>Nested</p>
    </section>
</div>
```

Only "Direct Child" becomes red.

# 8. Adjacent Sibling Selector (+)

Selects the immediately following sibling.
```css
h1 + p {
    color: green;
}
```
```HTML

<h1>Title</h1>
<p>Paragraph 1</p>

<p>Paragraph 2</p>
```

Only Paragraph 1 is selected because it comes immediately after <h1>.

# 9. General Sibling Selector (~)

Selects all following siblings.
```css
h1 ~ p {
    color: blue;
}
```
```HTML

<h1>Heading</h1>

<p>One</p>
<p>Two</p>
<p>Three</p>
```
All three paragraphs become blue.

# 10. Attribute Selector ([])

Selects elements based on their attributes.
```css
input[type="text"] {
    border: 2px solid blue;
}
```
```HTML

<input type="text">
<input type="password">
```

Only the text input is selected.

Other examples:
```css
a[target] { }

input[required] { }

img[alt] { }
```
