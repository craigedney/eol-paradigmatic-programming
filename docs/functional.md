# Functional Programming

1. **Pure Functions**: Functions always produce the same result for the same input and have no side-effects.

```typescript
// Pure function to calculate sum
const sum = (a: number, b: number): number => a + b;
```

2. **Immutable Data**: Avoiding change of existing data structures, instead, we create new ones.

```typescript
// Using the spread operator to create a new array instead of modifying the existing one
const appendToArray = (arr: number[], value: number): number[] => [...arr, value];
```

3. **First-class and Higher-order Functions**: Functions that take other functions as parameters or return them.

```typescript
// A higher-order function that takes a function as a parameter
const compute = (a: number, b: number, operation: (x: number, y: number) => number): number => operation(a, b);
```

4. **Functional Composition**: The process of combining two or more functions to produce a new function.

```typescript
const increment = (x: number): number => x + 1;
const double = (x: number): number => x * 2;

// Composing the two functions
const incrementAndDouble = (x: number): number => double(increment(x));
```

5. **Recursion**: Since we avoid loops in FP, recursion is the tool of choice for iterative operations.

```typescript
// Factorial using recursion
const factorial = (n: number): number => (n <= 1 ? 1 : n * factorial(n - 1));
```

Here's how you can use the above concepts in a simple Node.js program:

```typescript
    console.log(sum(5, 3)); // Outputs: 8
    console.log(appendToArray([1, 2, 3], 4)); // Outputs: [1, 2, 3, 4]
    console.log(compute(5, 3, sum)); // Outputs: 8
    console.log(incrementAndDouble(2)); // Outputs: 6
    console.log(factorial(5)); // Outputs: 120
```

More concepts:

- monads
- functors
- currying
