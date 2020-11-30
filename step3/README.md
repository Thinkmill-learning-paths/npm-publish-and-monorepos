# npm publish

## Step 3 - Creating a Monorepo

Many Thinkmill projects (particularly ones we publish to npm) exist in a monorepo. As such, knowing how to set up a monorepo is often important when you are publishing packages.

### What is a Monorepo?

For information on monorepos, and how Thinkmill thinks about them, we recommend reading through the contents on [our monorepo guide](https://monorepo.guide/).

### Completing this Excercise

To complete this excercise, you will need to set up a monorepo for use in Step 4. It will need to have the following packages:

```json
{
	"name": "@[your-scope]/learning-do-not-publish",
	"version": "1.0.0",
	"main": "src"
}
```

```json
{
	"name": "@[your-scope]/learning-test-package-1",
	"version": "1.0.0",
	"main": "src"
}

```

```json
{
	"name": "@[your-scope]/learning-test-package-2",
	"version": "1.0.0",
	"main": "src",
	"dependencies": {
		"@noviny/learning-test-package-1": "0.1.0"
	},
	"devDependencies": {
		"@noviny/learning-do-not-publish": "0.1.0"
	}
}
```

And add a `src/index.js` for each package.

Once you have the packages set up, you will want to add a `workspaces` field to the root `package.json`, and add `preconstruct` and `manypkg` into your project, following their own docs.

You will add changesets in during the next step.

NOTE: The configs I have given you will create errors - you will need to solve these
