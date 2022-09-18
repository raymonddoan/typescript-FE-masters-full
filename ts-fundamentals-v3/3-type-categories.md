# Type Categories

## Typing Functions

Avoid using `any` at all costs

## Typing Functions Q&A and objects

When `any` is passed into well typed code, this will cause the well-typed code to fail.

- It can masqerade as anything.

## Optional Properties

By providing ? in the variable (ie. variable?), then the function is asking for an optional property.
You can apply a type guard to make sure the value is provided.

```ts
if (typeof car.chargeVoltage !== "undefined")
    str += `// ${car.chargeVoltage}v`
```

NOTE: read the errors from the bottom up

## Index Signatures & Q&A

Error is shown when the variable is proven to be useless.

## Arrays & Tuples

