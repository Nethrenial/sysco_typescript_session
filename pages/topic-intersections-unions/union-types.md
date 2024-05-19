# Union of types

In TypeScript, we can combine multiple types into one using the `|` operator. This is called a union type. A union type is a type that can be one of several types. The resulting type will have all the properties and methods of all the types involved.To do this with interfaces, we can use the `extends` keyword.

```ts {monaco-run}
type A = { a: number; b: string }
type B = { b: number; a: string }
type C = A | B

const c1: C = { a: 1, b: "hello1" } // c1 must conform to either A or B
const c2: C = { b: 2, a: "hello2" } // c2 must conform to either A or B
const c3: C = { a: 3, b: 4 } // This will show error as c3 does not conform to either A or B

interface IA { a: number; b: string }
interface IB { b: number; a: string }
// but unlike types, interfaces can't be directly combined using the | operator
// instead, we can use type aliases to achieve the same effect
type IC = IA | IB

const ic1: IC = { a: 1, b: "hello1" } // ic1 must conform to either IA or IB
const ic2: IC = { b: 2, a: "hello2" } // ic2 must conform to either IA or IB
const ic3: IC = { a: 3, b: 4 } // This will show error as ic3 does not conform to either IA or IB
```