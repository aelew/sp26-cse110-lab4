# Part 2

1. Line 12 prints `3`. This is because `i` is declared using `var`, which is function-scoped instead of block-scoped. This causes `i` to not be confined to the scope of the `for` loop block and "leak" out to the function scope. After the `for` loop finishes, `i` holds the value that caused condition `i < prices.length` to fail, which is `3` (the length of the `prices` array).

2. Line 13 prints `150`. This is because of the same reason as question 1. `discountedPrice` is also declared using `var`, so it leaks out into the function scope. `discountedPrice` also holds the last value it was assigned from final iteration `i=2`, which is `300 * (1 - 0.5) = 150`.

3. Line 14 prints `150`, which is the last value of `finalPrice` after the loop finishes (`300 * 0.5 = 150`). `finalPrice` is a `var`, which is function-scoped, so it is still accessible after the loop ends.

4. The function returns `[50, 100, 150]`. Each price is multiplied by (1 - 0.5), rounded to 2 decimal places, and pushed into discounted, which is then returned.

5. Line 12 throws a reference error since `i` is not defined in the function scope. `i` is declared using `let`, which is block-scoped to the `for` loop and is therefore inaccessible outside of it.

6. Line 13 throws a reference error as well because `discountedPrice` is declared with `let` inside the `for` loop block, making it inaccessible outside of it.

7. Line 14 prints `150`. `finalPrice` is declared using `let` and holds the last value assigned during the `for` loop.

8. The function returns `[50, 100, 150]` (same as question 4). `discounted` is declared at the function level and is returned directly, so whether it is declared with `let` or `var` does not affect the returned value.

9. Line 11 throws a reference error since `i` is not defined in the function scope. `i` is declared using `let`, which is block-scoped to the `for` loop and is therefore inaccessible outside of it.

10. Line 12 prints `3`. This is because `length` is declared with `const` at the function level on line 4, so it's accessible outside the loop and holds the value of `prices.length`.

11. This function will return `[50, 100, 150]`. Like in question 4 and 8, `discounted` is declared at the function level and returned directly, so the const/let/var differences don't affect the return value.

12.

a. `student.name`

b. `student['Grad Year']`

c. `student.greeting()`

d. `student['Favorite Teacher'].name`

e. `student.courseLoad[0]`

13.

a. `'32'`
Since one side is a string, JS converts `2` into a string and concatenates them

b. `1`
The `-` operator is numeric only, so JS converts `'3'` into the number `3`

c. `3`
In numeric conversion, `null` becomes `0`, so this becomes `3 + 0`

d. `'3null'`
Since one side is a string, JS converts `null` into the string `'null'` and concatenates

e. `4`
`true` converts to `1`, so this becomes `1 + 3`

f. `0`
`false` converts to `0`, and `null` converts to `0`, so this becomes `0 + 0`

g. `'3undefined'`
Since one side is a string, JS converts `undefined` into the string `'undefined'` and concatenates

h. `NaN`
The `-` operator tries numeric conversion. `'3'` becomes `3`, but `undefined` becomes `NaN`, so the result is `NaN`

14.

a. `true`
JS converts `'2'` into the number `2`, and `2 > 1` is true

b. `false`
JS compares both of the values alphabetically/lexicographically since they are both strings. It compares the first characters: `'2'` is greater than `'1'`, so `'2' < '12'` is false

c. `true`
`==` allows type conversion, so `'2'` is converted into the number `2`

d. `false`
`===` does not allow type conversion. One value is a number and the other is a string

e. `false`
`true` converts to `1`, and `1 == 2` is false

f. `true`
`Boolean(2)` becomes `true` because nonzero numbers are truthy. Then `true === true` is true.

15.

`==` checks if the two values are equal after allowing type conversion.

`===` checks if the two values are equal without type conversion, so both the value and the data type must match for the comparison to be true.

16. See [part2-question16.js](./part2-question16.js)

17. Result: `[2, 4, 6]`

`modifyArray([1, 2, 3], doSomething)` passes the array `[1, 2, 3]` and the function `doSomething` into `modifyArray`. Inside of the `for` loop, each value in the array is passed into callback function `doSomething`. Each returned value gets pushed into `newArr`, which becomes `[2, 4, 6]`. Then `modifyArray` returns that new array.

18. See [part2-question18.js](./part2-question18.js)

19. Output:

```
1
4
3
2
```
