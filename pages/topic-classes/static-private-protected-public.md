# Classes: private, protected, public and static

In TypeScript, classes can have members that are private, protected, or public. These access modifiers control how the members of the class can be accessed from outside the class.
And static members are those that belong to the class itself, rather than to instances of the class.
This feature also exists in JavaScript.

```ts {monaco-run}
class Animal {
    // public members can be accessed from outside the class
    public name: string = "Max" // properties are public by default and the public keyword is optional
    // private members can only be accessed from within the class
    private age: number = 10
    // protected members can be accessed from within the class and its subclasses
    protected color: string = "Red"
    // static members belong to the class itself
    static numberOfAnimals = 0
}

class Dog extends Animal {
    tryAccessingMembers() {
        console.log(this.name) // public members can be accessed from within the class and anywhere else
        // console.log(this.age) // error: Property 'age' is private and only accessible within class 'Animal'
        console.log(this.color) // protected members can be accessed from within the class and its subclasses
        console.log(Animal.numberOfAnimals) // static members can be accessed from within the class and anywhere else
        // but you can't access private members from subclasses
        console.log(this.age) // error: Property 'age' is private and only accessible within class 'Animal'
    }
}

// let's try some usage of these classes to see what happens
```