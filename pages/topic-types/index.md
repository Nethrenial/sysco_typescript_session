
# Type Aliases

Define the structure of data or create new Types by utilizing existing types in various ways
You can edit the following code blocks to see the changes in the editor in real-time.Hover to see type information as well.
For example,

```ts {monaco-run}
// literal types
type PI = 3.14 // hover over PI to see the type, it says 3.14 instead of "number"
type Name = 'John' // hover over Name to see the type, it says 'John' instead of "string"

type Human = {
  name: string
  age: number
}

type DeveloperType1 = Human & {
  skills: string[]
}

type Skilled = { // or we can define yet another type describe anything with skills
  skills: string[]
}

type DeveloperType2 = Human & Skilled // and then we can use it in multiple places
```
