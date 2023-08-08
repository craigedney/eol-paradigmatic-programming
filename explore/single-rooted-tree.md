# Single-rooted Tree

The concept isn't a widely recognized programming paradigm like object-oriented, functional, or procedural programming. Typically, when discussing programming paradigms, a "single-rooted tree" isn't something that comes up.

However, the term can be familiar in the context of object-oriented programming with class hierarchies, especially in languages like Java, where all classes implicitly inherit from a single root object, `java.lang.Object`.

That said, JavaScript (and by extension, TypeScript) is prototype-based, meaning that objects can inherit directly from other objects without the traditional class-based hierarchy seen in languages like Java or C++. But all objects in JavaScript do have a root prototype, which is `Object.prototype`.

I'll provide an example where we might imagine a single-rooted hierarchy using TypeScript classes:

```typescript
// Root of our tree
class LivingBeing {
    breathe(): void {
        console.log("Breathing...");
    }
}

class Animal extends LivingBeing {
    move(): void {
        console.log("Moving...");
    }
}

class Bird extends Animal {
    fly(): void {
        console.log("Flying...");
    }
}

class Fish extends Animal {
    swim(): void {
        console.log("Swimming...");
    }
}

const eagle = new Bird();
eagle.breathe(); // From LivingBeing
eagle.move();    // From Animal
eagle.fly();     // From Bird

const salmon = new Fish();
salmon.breathe(); // From LivingBeing
salmon.move();    // From Animal
salmon.swim();    // From Fish
```

In this example:
- `LivingBeing` is the root. Everything is a `LivingBeing` and has the ability to breathe.
- `Animal` extends `LivingBeing`, meaning all animals are living beings and have the ability to move.
- `Bird` and `Fish` both extend `Animal`. This means all birds and fish are animals, but they have specialized movement abilities - birds can fly, and fish can swim.

This forms a single-rooted tree hierarchy:

```
LivingBeing
|
|-- Animal
    |
    |-- Bird
    |
    |-- Fish
```

It's essential to understand that while this demonstrates a class hierarchy, it's not necessarily a depiction of a "Single-rooted Tree programming paradigm" since such a paradigm isn't a standard or widely recognized term in the field of computer science or software engineering.


## Other terms
- Mono-rooted Hierarchical Structure
- Single-rooted Hierarchical Modular Structure
