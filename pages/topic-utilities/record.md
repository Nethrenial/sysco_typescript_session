# Record Utility Type

The `Record` utility type is used to create a new type by specifying the type of the keys and values.

```ts {monaco-run}
type Product = {
    name: string
    price: number
}
type ProductMap = Record<string, Product>
// to do this without Record,
type ProductMap2 = {
    [key: string]: Product
}
const products: ProductMap = {
    laptop: { name: 'Laptop', price: 1000 },
    mouse: { name: 'Mouse', price: 20 }
    keyboard: "keyboard" // error: Type 'string' is not assignable to type 'Product'
}
type StringNumberMap = Record<string | number, string | number>
// to do this without Record,
type StringNumberMap2 = {
    [key: string | number]: string | number
}
// usage
const map: StringNumberMap = {
    1: 'one',
    '2': 'two',
    '4': true // error: Type 'boolean' is not assignable to type 'string | number'
}
```