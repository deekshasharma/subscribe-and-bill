

# FAQs

## I don't see a `tsconfig.json` file in the project. Where is it?
- `ts-node` uses a default `tsconfig.json` when it cannot find one within the project directory. 
  To log the configuration being used, run the following on the CLI.

```shell
npx ts-node --show-config
```

To log node and typescript versions, type the command below.
```shell
npx ts-node -vv
```
**Note**: Since `ts-node` is installed locally, it should be used with `npx` prefix.

## How to start the app using our own `tsconfig.json` file?

Add the following in your `package.json` `start` script
```shell
    "start": "ts-node --project tsconfig.json src/index.ts",
```

## How to add a plugin to my current `eslint` configuration?
With ESLint, you can add a number of features to your config file via plugins. Please refer to [awesome-eslint](https://github.com/dustinspecker/awesome-eslint) to make your eslint configuration richer.
Currently, in this project we have only 2 rules in our `.eslintrc` file. 

1) To disallow `console.log` statements
2) To disallow the use of `for`, `for-in`, `while` and `do-while` loops. Instead, use `map` and `forEach`.

## Open questions | things to be done
- How will the output directory be generated with the JS files?
- Add Husky pre-commit hook for linting
- Add prettify

