# Pick Utility Type

The `Pick` utility type is used to create a new type by picking only a subset of properties from an existing type.

```ts {monaco-run}
type Product = {
    name: string
    price: number
    description: string
}
type Order = {
    id: number
    deliveryInfo: {
        address: string
        date: Date
    }
    products: Pick<Product, 'name' | 'price'>[]
}
const order: Order = {
    id: 1,
    deliveryInfo: {
        address: '123 Main St',
        date: new Date()
    },
    products: [
        { name: 'Laptop' }, // error: Property 'price' is missing, but won't complain about 'description'
        { name: 'Mouse', price: 20 }
    ]
} 
```