
### 1. Which color does the paragraph currently display? Explain why by identifying the CSS rule that wins and the principle that governs this (hint: think about the "weight" or priority of different selector types).


The paragraph currently displays in **red**.
The `#main-text` selector wins because ID selectors have higher specificity than class selectors and element selectors. In other words, CSS gives more "weight" to `#main-text` than to `.highlight` or `p`, so the paragraph becomes red.

### 2. Make the paragraph green - you may only add one new CSS rule, and you cannot use inline styles (e.g., style="..."). What selector did you use, and why does it override the others?

I used this selector:

```css
p#main-text.highlight {
    color: green;
}
```

This overrides the other rules because it is more specific. It combines an element selector (`p`), an ID selector (`#main-text`), and a class selector (`.highlight`) to target the same paragraph. Since this selector has more specificity than `#main-text`, `.highlight`, or `p`, its `color: green;` rule wins.

### 3. If you were forbidden from using an ID selector or inline styles, how else could you make the paragraph green by adding just one rule? (Hint: Combine selectors from the lesson).

If the existing `#main-text` rule stays in the CSS, a normal selector without an ID cannot override it by specificity alone. ID selectors have more weight than any combination of class and element selectors.

One way to make the paragraph green without using an ID selector or inline styles is:

```css
p.highlight {
    color: green !important;
}
```

The selector `p.highlight` combines the element selector `p` and the class selector `.highlight`, so it targets the paragraph. The `!important` part makes this declaration override the earlier `#main-text` rule, even though `#main-text` has higher specificity.
