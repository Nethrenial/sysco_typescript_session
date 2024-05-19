# Generic "types"

```ts {monaco-run}
type LnkedListNode<T> = {
  value: T
  next: LnkedListNode<T> | null
}
const node: LnkedListNode<number> = { 
// unlike functions, we need to specify the type argument, unless there's a default
  value: 1,
  next: {
    value: 2, // try using a string or any other non-number here to see the error
    next: null
  }
}
// example with default type argument
type LnkedListNodeWithDefault<T = number> = {
  value: T
  next: LnkedListNodeWithDefault<T> | null
}
// only need to specify the type argument if you want to use a different type
const nodeWithDefault: LnkedListNodeWithDefault = {
    value: 1,
    next: {
        value: 2,
        next: null
    }
}
```