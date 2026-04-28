# DevTools - Debugging

1. The bug is that the values of `num1` and `num2` in `calculateSum()` were being string-concatenated instead of added together as numbers.

2. A simple fix for this would be to convert `num1` and `num2` to numbers using `Number()` before adding them together.
