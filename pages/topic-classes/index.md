# Classes in TypeScript

In addition to the features in Javascript, typescript provides more features for OOP that resemble other OOP languages like Java, C# etc.

```ts {monaco}
// in typescript
class Person {
    name: string       
    private age: number
    protected gender: string
    constructor(name: string,gender: string ) {
        this.name = name
        this.gender = gender
        this.age = 0
    }
    setAge(age: number) {
        this.age = age;
    }
}
// here you will get excellent type support
const nethsara = new Person("Nethsara", "male")
nethsara.setAge(24)
console.log(nethsara)
// can't access age
console.log(nethsara.age) // hover to see error

// let's try out what "protected" does
```