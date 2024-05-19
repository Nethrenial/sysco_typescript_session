# Generic "classes"

```ts {monaco-run}
class Box<T> {
    contents: T[]
    constructor(contents: T[]) {
        this.contents = contents
    }
}
const box1 = new Box<string>(["apple", "banana", "cherry"])
// or without explicitly specifying the type
const box2 = new Box([1, 2, 3]) // hover over box2 to see the inferred type
// you can use this types to supply arguments for interfaces or types to implement as well
interface Container<T> {
    contents: T[]
}

class Crate<T> implements Container<T> {
    contents: T[]
    constructor(contents: T[]) {
        this.contents = contents
    }
}

// as in any other places using generics, you can specify multiple generic types as well as default types
```