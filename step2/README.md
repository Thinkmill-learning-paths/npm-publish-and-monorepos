# npm publish

## Step 2 - Publishing `dist` Instead of `source`

It is common when publishing to build your code, and then not publish the dist. This is because we often write our code in a format that is not natively readable, and node modules are not processed by client build systems.

Using the package that you published in exercise 1, add the following "build" script to the package.json. 

```json
"build": "cp src/index.js dist/index.js"
```

Note: as we are not learning about how to run build scripts as part of this module, this script will just copy index.js to dist.

Add an additional file to src called "only-in-src.txt". This will allow us to identify a difference between src and dist. 

The goal of this exercise it to:
- Have a build process to create dist files from `src/`
- If code was committed to the repository, the `src/` folder is committed, however the `dist/` folder is excluded
- When we publish the code, the `dist/` folder is published, but the `src/` folder is not.
- When inspecting an installed package (by looking in node_modules), it does not include the file "only-in-src.txt".
- You can install your package from `npm` and require it and it pulls in the expected file so you can still run:
    ```js
    const testString = require("@noviny/learning-test-package-1");
    
    // This should print out "Congratulations! You did it!"
    console.log(testString);
    ```
- Make sure you check that the `src` files are no longer being included from npm when you run your test.
