# Type narrowing

Type narrowing is a technique used to narrow down the type of a variable within a block of code. Even with inference, typescript is ususally able to determine types along decision paths. However, there are cases where TypeScript is unable to determine the type of a variable. 

```ts {monaco-run}
function func1(x: string | number) {
    if(typeof x === 'string') {
        x // string
    } else {
        x // number
    }
}

type Dog = { bark: () => void }
type Cat = { meow: () => void }
// or using methods or properties only available on a certain type
function func2(x: Dog | Cat) {
    if('bark' in x) {
        x // Dog (hover over x to see the type)
    } else {
        x // Cat (hover over x to see the type)
    }
}
```