# npm publish

## Step 1 - A Simple Publish

This task is to publish a package to npm.

Work inside the directory `/simple-package` or copy the directory's contents to a new project. 

Before publishing, update the scope in the package's name to your own npm username. This will allow you to publish to your own scope

Validate this works: 
* the published package can be installed in a new project
* running the following code with `node index.js`: 
 
    ```index.js
    const testString = require("[your scope]/learning-test-package-1");
    
    // This should print out "Congratulations! You did it!"
    console.log(testString);
    ```
    
    prints "Congratulations! You did it!".
    

## Bonus Tasks

- Publish a new version after your initial publish
- Add a tag to your package
- Open up your `node_modules` and look at the file contents that you have pulled down from `npm`
