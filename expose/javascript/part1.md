# Part 1

1. Line 9 prints:
```
values added:  20
```

2. Line 13 prints:
```
final result:  20
```

3. We shouldn't use `var` because variables leak out of blocks, which can cause unintended access. `var` declarations are also hoisted and initialized as `undefined`, hiding potential bugs. Declaring the same variable twice also won't throw an error, so doing so could go unnoticed. It's better to use `const` by default and `let` if we need to reassign the value.

4. Line 9 prints:
```
values added:  20
```

5. Line 13 throws a reference error because `result` is not defined. This is because `let` is scoped to the block it's declared in (the `if` block). Once execution exits that block and reaches line 13, `result` has already become out of scope and is inaccessible.

6. Line 9 is never reached because an error occurs on line 7. Line 7 tries to reassign a value to `result` after its initial declaration, which is not allowed since `result` is declared as `const` in this code snippet.

7. Line 13 is also never reached in this code snippet because the program would already crash on line 7.
