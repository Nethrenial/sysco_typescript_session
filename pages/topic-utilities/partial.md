# Partial utility type

The `Partial` utility type allows you to make all properties of a type optional. This is useful when you want to create a new type that has the same properties as an existing type, but you want to make some of the properties optional.


```ts {monaco-run}
type CreateProductDTO = {
    name: string
    price: number
    description: string
}

type UpdateProductDTO = Partial<CreateProductDTO> // hover over to see the difference

const newProduct: CreateProductDTO = {
    name: 'Laptop',
    price: 1000,
    description: 'A laptop'
}

const updatedProduct: UpdateProductDTO = { // here you can enter any subset of properties, even none
    name: 'Laptop'
}
```