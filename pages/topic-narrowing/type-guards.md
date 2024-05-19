# Type Guards

Type guards are a way to check the type of a variable at runtime. They are useful when working with union types.

```ts {monaco-run}
type Fish = { swim: () => void }
type Bird = { fly: () => void }

function isFish(pet: Fish | Bird): pet is Fish {
  /*
  This is a type predicate. It returns a boolean value that tells TypeScript whether the pet is a Fish or not.It's rusable and can be used in other functions and recommended over using "in" operator.
   */
  return (pet as Fish).swim !== undefined;
}

function move(pet: Fish | Bird) {
  if (isFish(pet)) {
    pet.swim();
  } else {
    pet.fly();
  }
}

const goldFish = { swim() { console.log('swimming') } }
move(goldFish)
const parrot = { fly() { console.log('flying') } }
move(parrot)
```