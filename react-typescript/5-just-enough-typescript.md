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

Keys and Values

- `keyof` gives all the keys of the provided type
- `Obj[keyof Obj]` will give you all the values of the object

Unions & Intersections

- Unions of Objects will only give the shared prop. Unions of Types will give everything.
- Intersection of Objs will give the combination of the two. Intersection of Types will give the shared values.

Conditionals

Exclude & Extract (Used for the Union Members)

Pick (similar to lodash) & Omit (Used for Types / Objects)

- Picks out all the keys of the type
- Omit is the opposite and will leave out the listed keys

`React.HTMLProps<HTMLXXXElements>`

`React.ComponentProps<typeof XXX>`

- Will give you in the prop within the component and pull that out

## Refactoring in Utility Types

## Template Literals


