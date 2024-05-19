
# Interfaces

Define the structure of data (Same as Types) or create new Types by utilizing existing types in various ways
However, Interfaces cannot be used to define unions, intersections, or other types of relationships.
But they can be extended to create new interfaces.
Also "Types" can use interfaces in intersections and unions.

```ts {monaco-run}
interface Human {
  name: string
  age: number
}

interface DeveloperInterface1 extends Human { // extends can be used to create new interfaces
  skills: string[]
}

interface Skilled { // or we can define yet another interface describe anything with skills
  skills: string[]
}

interface DeveloperInterface2 extends Human, Skilled {} // and then we can use it in multiple places
```
