# More examples of interfaces

```ts {monaco-run}
interface AnimalLike { // here, this interface can be thought of as something that describes an animal-like thing
    makeSound: () => void
}
// using AnimalLike interface to define a Dog class
class Dog implements AnimalLike { // saying implements AnimalLike means that Dog is an AnimalLike and must have the properties and methods defined in AnimalLike, but it can have more properties and methods
    breed: string
    constructor(breed: string) {
        this.breed = breed
    }
    makeSound() { console.log('Woof') }
}

// because Dog implements AnimalLike, we can use it anywhere AnimalLike is expected, example
function makeSound(animal: AnimalLike) {
    animal.makeSound()
}

makeSound(new Dog('Labrador')) // prints 'Woof'

// however we can't use any other objects that implement AnimalLike somewhere that expects a Dog (just like in OOP)
```
