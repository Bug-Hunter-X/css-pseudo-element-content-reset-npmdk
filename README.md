# CSS Pseudo-element Content Clearing Bug

This repository demonstrates a subtle bug in CSS where the content of a pseudo-element (::before) is unexpectedly cleared due to conflicting styles and specificity.  The problem arises when a more specific rule unintentionally overrides the initial content set for the pseudo-element.

## Bug Description
The main issue lies in the specificity of CSS selectors.  While the `::before` pseudo-element initially has content assigned, a seemingly unrelated hover style (with higher specificity) accidentally clears that content because it also includes a `content` property with an empty string. 

## Solution
The solution involves adjusting the CSS to avoid the conflict and ensure the pseudo-element content is correctly displayed.  The fix prioritizes the `::before` content property either through increased specificity or by refactoring the CSS structure to avoid the unwanted override.

## How to reproduce:
1. Open `bug.css`
2. Open `solution.css` to compare the solutions
3. Observe the behavior of the pseudo-element's content in each example.