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

In this HTML, the first paragraph is the first child inside `.container`, so this selector would work:

```css
.container p:nth-child(1) {
    color: purple;
}
```

However, `p:nth-child(1)` by itself could also target any other paragraph on the page that is the first child of its own parent. Adding `.container` makes the selector more specific to this section.

If there were another element before the first paragraph, like a heading, then `p:nth-child(1)` would not target the paragraph anymore because the paragraph would no longer be the first child.
