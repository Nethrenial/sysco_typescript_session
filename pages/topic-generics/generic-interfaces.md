# Generic "interfaces"

```ts {monaco-run}
interface Farm<AnimalType> {
    animals: AnimalType[]
    addAnimal(animal: AnimalType): void
}
interface Dog { // or you can use a type here
    bark(): void
}
class DogFarm implements Farm<Dog> {
    animals: Dog[] = [] // try using a different type here to see the error
    addAnimal(animal: Dog) { // try using a different type here to see the error
        this.animals.push(animal)
    }
}

interface GoldenRetriever extends Dog {
    fetch(): void
}

class GoldenRetrieverFarm implements Farm<Dog> {
    animals: GoldenRetriever[] = [] // however, you can use any type/interface that extends Dog here
    addAnimal(animal: GoldenRetriever) { // however, you can use any type/interface that extends Dog here
        this.animals.push(animal)
    }
}
```