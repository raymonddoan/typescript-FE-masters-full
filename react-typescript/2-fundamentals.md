# Fundamentals

## Types vs Interfaces

- Similar to function declaration vs function expression
  - declaration revolves around hoisting
- Treat the rest arguments as arrays of a data type

## Typing Children

When passing through children, then options for the data type are:

- JSX.Element;
  - Only works for when there is only 1 child
- JSX.Element | JSX.Element[];
  - Doesn't work because the original element is an element, but not a string (??)
- **React.ReactNode;**
  - Most correct - Anything that would work as a child since a React component will always be a node.
  - Difference between ReactNode vs ReactElement:
    - ReactElement: A ReactElement is an object with a type and props.
    - ReactNode: A ReactNode is a ReactElement, a ReactFragment, a string, a number or an array of ReactNodes, or null, or undefined, or a boolean.
- React.ReactChildren;
  - Accepts an array of children, but not a single child
  - Not a particular type
- React.ReactChild[];
  - Accepts an array of children, but not a single child
  - Subset of ReactNode

## Typing CSS Styling

- Hover over variables to get the valid types
- **React.CSSProperties** is the type for CSS properties in TS
- You would still have the style as a prop, but since some components do not require styling, then you should have the ? operator

## useState Hook

- When the data type is original set, TS will know to hold that state until the end
