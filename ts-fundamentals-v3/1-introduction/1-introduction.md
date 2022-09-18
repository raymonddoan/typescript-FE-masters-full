# Introduction

There are three parts to Typescript:

- Language
- Language Server: software outside Typescript
- Compiler: analyses the code base

## Why developers want types

- Leaves the developers' intent "on the page"

**But how?**

1. Removes the guesswork on what are the constraints, what is the function supposed to do, etc.
2. Has potential to move some errors from *runtime* (which affects users) to *compile-time* (which developers can resolve within pull requests)
3. Serves as a function for *great code authoring* experience (rich editing environment)

For Point #2, errors mentioned include:

- Values that are potentially absent (`null` or `undefined`)
- Incomplete refactoring
- Breakage around *internal code contracts*
