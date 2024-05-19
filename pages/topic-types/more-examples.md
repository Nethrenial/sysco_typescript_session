# More examples of types

You saw an example with using it for object types, but "type" can be used to type literally anything in TypeScript.

```ts {monaco-run}
// For example,
type Birthday = string | Date // Birthday can be a string or a Date
type OnClickHandler = (event: MouseEvent) => void // OnClickHandler is a function that takes a MouseEvent and returns void
type Birthdays = Birthday[] // Birthdays is an array of Birthdays
// example of composing multiple types to create a larger type
type Product = {
  name: string
}
type Order = {
    deliveryInfo: {
        address: string
        date: Date
    }
    products: Product[]
}
async function getOrders() {
    return [] as Order[]  // hover over the function to the the type definition of this function
}

async function displayOrder() {
    const orders = await getOrders()
    orders.forEach(order => {
        console.log(order) // hover over order to see the amazing type information
    })
}

```
