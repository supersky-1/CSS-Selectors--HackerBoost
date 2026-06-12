## CSS Selectors Exercises Summary

This project helped me practice different CSS selectors and understand how they affect HTML elements. Each exercise focused on a different selector concept, from specificity to pseudo-classes and nested selectors.

### Exercise 1: The Specificity Showdown

In this exercise, I compared element, class, and ID selectors that were all trying to style the same paragraph. I learned that ID selectors have more specificity than class selectors and element selectors, so `#main-text` won over `.highlight` and `p`. I also practiced creating a more specific selector like `p#main-text.highlight` to override earlier rules.

### Exercise 2: The Grouping and Nesting Debug

In this exercise, I fixed selectors that were too broad or written incorrectly. I learned how to use descendant selectors like `nav a`, group selectors like `h2, h3`, and child selectors like `ul.main-list > li`. I also learned that a selector can still affect more elements than expected if multiple parts of the HTML share the same class.

### Exercise 3: Target Practice Logic Puzzle

In this exercise, I used pseudo-classes and descendant selectors to target specific elements. I used `:nth-child(2)` to target only "Item 2", `:last-child` to style the second paragraph, and `.container p` to style both paragraphs inside the container. I learned that `:nth-child()` is based on an element's position inside its parent, not just its tag name.

### Exercise 4: Interactive Profile Card

In this exercise, I styled a small profile card with grouped selectors, button styling, and form input states. I used `:hover` to change the button when the user moves over it and `:focus` to change the input border when the user clicks into it. I learned how pseudo-classes can make a page feel more interactive.

### Exercise 5: Predict the Output

In this exercise, I predicted which CSS rules would apply based on inheritance, the universal selector, and specificity. I learned that a direct rule from `*` can beat an inherited rule from a parent, but a class selector like `.highlight` beats the universal selector because it has higher specificity.

### Exercise 6: Reconstruct from Scratch

In this exercise, I built a simple news sidebar from scratch. I used a `.sidebar` container, a heading, and a list of news links. I styled only the links inside the sidebar with `.sidebar a` and added a `:hover` effect so the links change color when the user moves over them. I learned how to combine structure and selectors to style a specific section of a page.
