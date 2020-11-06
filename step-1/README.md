# A Simple Publish

For this lesson, we are going to publish a package to npm. We have created a very simple package in the folder `/simple-package` in this repository.

You should clone this repository, or copy the two files from that repository across to your own folder.

Before you can publish, you will need to change the package's name. I recommend changing the scope to your own github username.

You can show that you have succeeded if, in a different project, you can run

```
yarn add @noviny/learning-test-package-1
```

except with your package name, and then if you write and run the file:

```js
const testString = require("@noviny/learning-test-package-1");

// This should print out "Congratulations! You did it!"
console.log(testString);
```

it prints out the string as expected.

## Bonus Tasks

- Publish a new version after your initial publish
- Add a tag to your package
- Open up your `node_modules` and look at the file contents that you have pulled down from `npm`
