## SCENARIO A
###    What color is the text inside the `<p>`? 
The text is orange

### Explain your reasoning. Does the universal selector * apply to the `<p>`? Does it inherit from the `div`? Which mechanism wins?

The universal selector `*` does apply directly to the `<p>`, so the paragraph gets:

```css
color: orange;
```

The `div` rule gives the parent `<div>` a blue color:

```css
div {
    color: blue;
}
```

The paragraph could inherit `color: blue` from the `<div>`, but inheritance only matters when the paragraph does not have its own direct color rule. Since `*` directly targets the `<p>`, the direct `color: orange;` wins over the inherited blue color.

So the text inside the `<p>` is **orange**

## SCENARIO B

### What color is the text?

If the text element has the class `highlight`, the text is **green**.

```css
* {
    color: purple;
}

.highlight {
    color: green;
}
```

### Why doesn't the universal selector `*` override the class selector? What principle does this demonstrate?

The universal selector `*` applies to every element, but it has the lowest specificity. The class selector `.highlight` is more specific, so it wins over `*`.

This demonstrates the principle of **CSS specificity**: selectors with more specific targeting have more weight in the cascade.
