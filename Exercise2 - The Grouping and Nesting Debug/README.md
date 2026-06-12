### 1. The a rule removes underlines from all links on the page. Rewrite the selector so it only targets links inside the `<nav>`.

Rewrite the selector like this:

```css
nav a {
    text-decoration: none;
}
```

This targets only `<a>` elements that are inside the `<nav>` element. The original selector, `a`, targets every link on the page, but `nav a` is more specific because it only applies to links nested inside the navigation section.

### 2. The `h2 h3` rule does not work. What is this selector actually trying to find? Rewrite it as a proper group selector so it styles both `<h2>` and `<h3>`.

The selector `h2 h3` is a descendant selector. It tries to find an `<h3>` element nested inside an `<h2>` element.
That does not work here because the `<h2>` and `<h3>` are separate elements. To style both headings, use a group selector with a comma:

```css
h2, h3 {
    color: navy;
}
```

The comma means "select both `h2` elements and `h3` elements."

### 3. The ul.main-list li rule makes all li elements bold. Rewrite it using the Child Selector (>) so it only targets direct children of ul.main-list. (Wait, does this actually fix the issue for both lists? Test it or trace the HTML tree to explain your reasoning).

Rewrite it like this:

```css
ul.main-list > li {
    font-weight: bold;
}
```

The `>` is the child selector. It only targets `<li>` elements that are direct children of a `<ul class="main-list">`.

However, this does not fully fix the issue in this HTML because both lists use the same `main-list` class:

```html
<nav>
    <ul class="main-list">
        ...
    </ul>
</nav>

<section>
    <ul class="main-list">
        ...
    </ul>
</section>
```

In both lists, the `<li>` elements are direct children of `ul.main-list`, so both lists still become bold. To target only the navigation list, the selector would need to be more specific, like this:

```css
nav ul.main-list > li {
    font-weight: bold;
}
```
