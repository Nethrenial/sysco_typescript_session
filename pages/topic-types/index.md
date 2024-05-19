
# Types

Define the structure of data or create new Types by utilizing existing types in various ways
You can edit the following code blocks to see the changes in the editor in real-time.Hover to see type information as well.
For example,

```ts {monaco-run}
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
