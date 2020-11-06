# npm publish

## Step 2 - Publishing `dist` Instead of `source`

It is common when publishing to build your code, and then not publish the dist. This is because we often write our code in a format that is not natively readable, and node modules are not processed by client build systems.

The goal of this exercise it to take the package that you published in exercise 1, and adjust it so that:

- We have a build process to create dist files from our `src/`
- if code was committed to the repository, the `src/` folder is committed, however the `dist/` folder is excluded
- When we publish the code, the `dist/` folder is published, but the `src/` folder is not.
- You can install your package from `npm` and require it and it pulls in the expected file so you can still run:

```js
const testString = require("@noviny/learning-test-package-1");

// This should print out "Congratulations! You did it!"
console.log(testString);
```

NOTE: As we are not learning about how to run build scripts as part of this module, you can have a 'build' script that is simply:

```json
"build": "cp -r src dist"
```

- Make sure you check that the `src` files are no longer being included from npm when you run your test.

## Bonus
