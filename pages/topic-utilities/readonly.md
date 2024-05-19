# Readonly Utility Type

The `Readonly` utility type is used to make all properties of a type read-only.

```ts {monaco-run}
type Product = {
    name: string
    price: number
}

const product: Readonly<Product> = {
    name: 'Laptop',
    price: 1000
}

product.name = 'Mouse' // error: Cannot assign to 'name' because it is a read-only property
```