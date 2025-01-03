# Silent Failure of CSS `content` Property with Relative URLs

This repository demonstrates a subtle bug related to the CSS `content` property when used with relative URLs within pseudo-elements (`::before`, `::after`).  If the relative path specified is incorrect or inaccessible, the browser won't throw an error; instead, the generated content simply won't appear.

The `bug.css` file contains the problematic CSS. The `bugSolution.css` file offers a corrected version.

**Problem:** Using a relative URL in the `content` property that the browser can't resolve leads to no visible error, making debugging difficult. 

**Solution:** Ensure that the relative URLs in the `content` property are correct and point to accessible resources relative to the CSS file's location.  Consider using absolute URLs for better reliability.