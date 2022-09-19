# Just Enough Typescript

## Generics

TS will try to figure out what the type will be.

Generics are powerful to allow the data passed back to be type-safe in the rest of the application.

Below is my version: (Con is that )

```ts
const tap = (numbers: number[], fn: (array: number[]) => number | undefined ) => {
  return fn(numbers)
};

const arrayWithoutLast = tap([1, 2, 3, 4], function (array) {
  // Pop always returns the value it removed from the end of the array.
  return array.pop();
});
```

If using arrow functions: (Note: Newer typescript compilers also support trailing comma `const foo = <T,>(x: T) => x;` to sidestep the JSX ambiguity)

```ts
const tap = <T,>(arg: T, fn: (x: T) => void): T => {
  fn(arg);
  return arg;
};
```

In normal functions:

```ts
function tap<T,>(arg: T, fn: (x: T) => void): T {
  fn(arg);
  return arg;
};
```


## Utility Types in React

## Refactoring in Utility Types

## Utility Types

## Template Literals
