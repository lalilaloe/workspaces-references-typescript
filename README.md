# workspaces-references-test

In this example we combine [npm workspaces](https://docs.npmjs.com/cli/v7/using-npm/workspaces) and [Typescript project references](https://www.typescriptlang.org/docs/handbook/project-references.html) to "structure your TypeScript programs into smaller pieces"

## Usage
This is a barebones template, you can simply test it using:

```
npm run build
npm start
```

### Project references

Normally you would use `tsc` as build script, with project references keep in mind that you need to use `tsc --build` or `tsc -b` in order to include references. The `composite` [property in tsconfig](https://www.typescriptlang.org/tsconfig#composite), defines the root of your package/module.

### Workspaces

Using [workspaces](https://docs.npmjs.com/cli/v7/using-npm/workspaces) unlocks some features that you can benifit from. For example to run scoped scripts `npm run test --workspace=backend`. You can also scope your packages, for example `npm init --scope @app -w ./libs` then you can use `@app/libs` to import for example. Read more on workspaces at [workspaces docs](https://docs.npmjs.com/cli/v7/using-npm/workspaces)