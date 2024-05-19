# Implementing types and interfaces

We can use "implements" to enforce that a class implements an interface or a type. This is useful when we want to ensure that a class has a specific set of properties and methods.

```ts  {monaco-run}
interface Animal {
    name: string
    makeSound(): void
}
class Dog implements Animal {
    name = "Max"
    makeSound() {
        console.log('Woof!')
    }
}
// try omitting the makeSound method to see the error
// we can also implement multiple interfaces
interface CanEat {
    eat(): void
}
class Cat implements Animal, CanEat {
    name = "Whiskers"
    makeSound() {
        console.log('Meow!')
    }
    eat() {
        console.log('Eating fish')
    }
} // try omitting methods to see the error
// you can also use a type instead of an interface
```