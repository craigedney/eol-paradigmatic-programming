# Structured programming

Use of structured control flow mechanisms (like loops and conditionals) and the organization of code into modular units. It's aimed at improving the clarity, quality, and development time of a computer program by using these subroutines, block structures, and loops.

Here's an example in TypeScript/Node.js that highlights the main concepts of Structured Programming:

1. **Sequential Execution**: Code is executed line by line, in order.

2. **Control Structures**: Commonly involves conditionals (`if-else`, `switch`) and loops (`for`, `while`).

3. **Subroutines/Modularity**: Break down the code into smaller, reusable functions or modules.

```typescript
// Sequential Execution
let x: number = 5;
let y: number = 10;
let result: number = 0;

// Subroutine to add two numbers
function add(a: number, b: number): number {
    return a + b;
}

// Subroutine to subtract two numbers
function subtract(a: number, b: number): number {
    return a - b;
}

// Control Structure (Conditional)
if (x > y) {
    result = subtract(x, y);
} else {
    result = add(x, y);
}

// Control Structure (Loop)
for (let i = 0; i < 3; i++) {
    console.log(`Loop iteration ${i + 1}`);
}

console.log(`Result: ${result}`);
```

In the above code:

- We begin with sequential execution by initializing variables.
- We define two subroutines: `add` and `subtract`, which represent modularity in our code.
- We then use a conditional (`if-else`) structure to decide which subroutine to call based on the relationship between `x` and `y`.
- Lastly, we use a `for` loop as an example of a control structure for iteration.
