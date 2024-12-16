# Unexpected Width Calculation using calc() with Percentages in CSS

This repository demonstrates a common, yet subtle, error when using the `calc()` function in CSS with percentage values.

The issue arises when combining percentages within a `calc()` expression.  While `calc(50% - 10px)` works predictably,  `calc(50% - 10%)` can yield unexpected results because the second percentage is relative to the element's computed width which is influenced by the calculation itself. This creates a circular dependency.

## Reproducing the Bug

1. Examine the `bug.css` file to see the incorrect implementation.
2. Observe the unpredictable layout in the browser.

## Solution

Refer to `bugSolution.css` for the corrected implementation. Avoid using percentages directly within `calc()` to avoid this unexpected calculation issue.