# Advanced Component Patterns

## Limiting Props a Component Can Take Based on Other Props

Limit the props by using the `never` data type so that it is type-safe.

## Polymorphic Components with TypeScript

Base components can be type safe as well.

[Example](./react-and-typescript-projects/projects/as-props/src/Application.tsx)

## Function Overloads

- Multiple type declarations for the same function.
- Actual implementation needs to appease all the overload functions.

## Demanding Props Based on Other Props

- Function overloads require you to do function declaration.
  - Function declaration is good for hoisting and debugging
- Reduces the edge cases can be done using function overloads.

## Solving for Context API Edge Cases

- `as const` means the returned value will be a read-only array.
