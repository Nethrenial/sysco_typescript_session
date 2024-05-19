# Generics

In typescript, generics are a way to create reusable types/interfaces/functions/classes that can work with any type.First of all let's consider generics with functions.

```ts {monaco-run}
/* syntax for defining a generic function
function functionName<T, ...other typeArguments>(arg: T // or multiple args, or even none): T // or any return type {
    // function body
}
*/
function identity<T>(arg: T): T {
    return arg
}
let num = 123
const output2 = identity(num) // output2 is of type number, because num is let and not const

interface Person { // or you can use a type here
    name: string
}
const person: Person = { name: 'John'}
const output3 = identity(person) // hover over output to see the type
/* Usually, it's not required to explicitly specify the type argument, 
but there are certain cases where it's necessary.For an example,
*/
const emailElement = document.querySelector<HTMLInputElement>('input#email-input') 
/*
Try calling methods on emailElement to see the intellisense and try removing the type argument to see the difference
*/

```
