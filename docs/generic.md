# Generic programming

Designing algorithms and data structures in a way that their functionality can work over multiple data types without depending on those data types. In TypeScript, this is primarily achieved using generics, which allow you to write classes, interfaces, and functions that work with different types in a type-safe manner.

Here's a TypeScript/Node.js example that highlights the main concepts of Generic Programming:

1. **Generic Function**: A function that can operate on data of various types.

2. **Generic Class**: A class structure that can be used with different types.

3. **Generic Interface**: An interface that can represent operations on various types.

```typescript
// Generic Interface
interface Pair<T> {
    first: T;
    second: T;
}

// Generic Function to print pairs
function printPair<T>(pair: Pair<T>): void {
    console.log(`First: ${pair.first}, Second: ${pair.second}`);
}

// Generic Class to store and retrieve data
class Storage<T> {
    private items: T[] = [];

    add(item: T): void {
        this.items.push(item);
    }

    get(index: number): T {
        return this.items[index];
    }
}

// Usage
const numberPair: Pair<number> = { first: 1, second: 2 };
printPair<number>(numberPair); // Outputs: First: 1, Second: 2

const stringPair: Pair<string> = { first: "Hello", second: "World" };
printPair<string>(stringPair); // Outputs: First: Hello, Second: World

const numberStorage = new Storage<number>();
numberStorage.add(5);
console.log(numberStorage.get(0)); // Outputs: 5

const stringStorage = new Storage<string>();
stringStorage.add("TypeScript");
console.log(stringStorage.get(0)); // Outputs: TypeScript
```

In the above code:

- We define a `Pair` interface with a generic type `T`. This means it can represent pairs of any type, whether numbers, strings, or even custom objects.
- The `printPair` function takes a generic type and prints a pair of that type.
- We also have a `Storage` class that can store items of any type. The type is provided when we create an instance of the class.
- Finally, we demonstrate how to use these generic structures with both number and string types.

The benefit here is that we have a single, unified implementation for different types, but still maintain type safety. You can extend this example by adding more complex types and operations, and the generic constructs will ensure type safety throughout.
