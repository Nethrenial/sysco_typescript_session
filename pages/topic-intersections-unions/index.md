# Intersection of types

In TypeScript, we can combine multiple types into one using the `&` operator. This is called an intersection type. An intersection type is a combination of two or more types. The resulting type will have all the properties and methods of all the types involved.To do an equivalent of this with interfaces, we can use the `extends` keyword.

```ts {monaco-run}
type A = { a: number }
type B = { b: string }
type C = A & B

const c: C = { a: 1, b: 'hello' } // c must have both properties of A and B

interface IA { a: number }
interface IB { b: string }
interface IC extends IA, IB {}

const ic: IC = { a: 1, b: 'hello' } // ic must have both properties of IA and IB

function returnC(a: A, b: B) {
    return { ...a, ...b }
}
// typescript is smart enough to know return value conforms to C
const returnedC: C = returnC({ a: 1 }, { b: 'hello' })
```