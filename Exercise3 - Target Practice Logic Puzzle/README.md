### 1. Target only "Item 2" to make it gray, using a pseudo-class.

I used the `:nth-child()` pseudo-class:

```css
ul li:nth-child(2) {
    color: gray;
}
```

This works because "Item 2" is the second `<li>` inside the `<ul>`.

### 2. Target only the "Second paragraph in container" to give it a background color, using a pseudo-class.

I used the `:last-child` pseudo-class:

```css
.container p:last-child {
    background-color: yellow;
}
```

This works because the second paragraph is the last child inside the `.container` element.

### 3. Target both paragraphs inside the .container to give them a line-height of 1.6, using a descendant selector.

Use this descendant selector:

```css
.container p {
    line-height: 1.6;
}
```

This works because `.container p` selects every `<p>` element that is inside the element with the class `.container`. Both paragraphs are inside the `.container` `<div>`, so both paragraphs get the `line-height: 1.6;` style.

### 4. Challenge: Why can't you easily target only the first paragraph using p:nth-child(1) in this specific HTML structure? Explain what p:nth-child(1) is actually looking for.

The selector `p:nth-child(1)` looks for a `<p>` element that is the first child of its parent.

It does not mean "the first paragraph." It means "a paragraph that is also child number 1."

In this HTML, the first paragraph is not the first child inside `.container` anymore because the `<h2>` comes before it:

```html
<div class="container">
    <h2>Introduction</h2>
    <p>First paragraph in container.</p>
    ...
</div>
```

Because of that, this selector would not work:

```css
.container p:nth-child(1) {
    color: purple;
}
```

The selector is looking for a `<p>` that is child number 1, but child number 1 is the `<h2>`, not the paragraph.

To target the first paragraph in this updated HTML, a better selector would be:

```css
.container p:first-of-type {
    color: purple;
}
```

This works because `:first-of-type` looks for the first `<p>` element of its type inside the parent, even if another element like `<h2>` comes before it.
