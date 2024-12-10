# Inconsistent Styling with :nth-child and Dynamic DOM Updates

This repository demonstrates a common issue with the CSS `:nth-child` selector when the Document Object Model (DOM) is dynamically updated.  The `:nth-child` selector's index is relative to its position in the DOM, meaning that adding or removing elements will change which elements match the selector.

**The Problem:**

The provided `bug.css` styles list elements using `:nth-child(odd)`.  However, if you interact with the dynamically-updated list (add or remove elements) the styling may become incorrect because the selector's indices are recomputed based on the modified DOM structure.

**The Solution:**

`bugSolution.css` showcases a solution. It avoids relying on `:nth-child` for dynamic styling, offering more robust and predictable results.  It uses JavaScript to apply styles based on a more resilient method, such as assigning unique identifiers or utilizing a class-based approach.