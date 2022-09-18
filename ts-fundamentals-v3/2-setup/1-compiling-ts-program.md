# Compiling a TS program

- `.d.ts` = declaration file, which contains only type information
- `tsc` = Typescript compiler
  - This will strip out the types from the `.ts` files into a `.d.ts` file and have the remaining code within the `.js` file
  - This is useful because it allows standard JS devs to compile the program with just the `.js` file

## package.json

- `tsc`
- `--watch` - watches the changes when a file saves (similar to `nodemon`)
- `--preserveWatchOutput` - stops every save from removing the console output

## tsconfig.json

- `include` - refers to which files folder you want to compile
- `compilerOptions`
- `outDir` - refers to where the output will be
- `target` - describes the langauge level of the output

It is also possible to pass everything from the `compilerOptions` to the `tsc` CLI as a flag. However it is best to do all in `tsconfig.json` file

NOTE: For use case where you are required to build and have an app that works on new browsers and have to have it operate on legacy browsers:

1. Have the `target` in `tsconfig.json` direct to the latest version, so that it works on the latest browsers
2. Then use `babel` to load it for the legacy browsers

## node

If we decide to just run `node` on the compiled JS file, it will break and throw an error. This is because it expects CommonJS modules.
To resolve this, we are required to add `"module": "CommonJS"` into the `tsconfig.json` file.
In doing so, this will convert `export` into `exports.<function> = <function>`
