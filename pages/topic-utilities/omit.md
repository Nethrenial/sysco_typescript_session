# Omit Utility Type

The `Omit` utility type is used to create a new type by omitting a subset of properties from an existing type.This is one of the most useful utility types in TypeScript, specially when working with 3rd party libraries.

```ts {monaco-run}
type Product = {
    id: number
    name: string
    price: number
    description: string
    quantity: number
    createdAt: Date
    updatedAt: Date
    isActive: boolean
}

type ProductDTO = Omit<Product, 'id' | 'createdAt' | 'updatedAt' | 'isActive'>

const newProduct: ProductDTO = { 
    /* ts won't complain about missing 'id', 'createdAt', 'updatedAt' or 'isActive', 
    but will complain about missing 'quantity'
    */
    name: 'Laptop',
    price: 1000,
    description: 'A laptop',
}
```