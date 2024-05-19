# Required Utility Type

The `Required` utility type is used to make all properties of a type required. It is the opposite of the `Partial` utility type.

```ts {monaco-run}

type OptionalProduct = {
    name?: string
    price?: number
    description?: string
}

type RequiredProduct = Required<OptionalProduct> // hover over to see the difference

const optionalProduct: OptionalProduct = { // can have any subset of properties
    name: 'Laptop'
}

const product: RequiredProduct = { // must have all properties
    name: 'Laptop',
    price: 1000,
    description: 'A laptop'
}
```
