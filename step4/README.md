# npm publish

## Step 4 - Publishing in a Monorepo

This exercise uses the monorepo we created in Step 3.

Many Thinkmill projects (particularly ones we publish to npm) exist in a monorepo. As such, knowing how to publish from a monorepo is an important extra step. Monorepos present extra interesting challenges to publishing:

1. Logistically, going in to each package and running a build script and then a publish script is very inefficient
2. You may not want to publish every package every time, meaning going in to each package to publish can lead to errors
3. There may be inter-dependencies between packages, and publishing one may mean you should also publish a second, but you may want to update the dependency of the second package. (this sentence is too dense)
4. Some packages are private, and you need to understand how to ensure these private packages are NOT published

Thinkmill has invested in a tool that helps manage this complexity - [changesets](https://github.com/atlassian/changesets).

To complete this exercise you need to:

- Be able to update the versions of multiple packages at once, after changes are made.
- Update the script `release` to version and publish the packages.

We recommend using changesets, but you can also experiment with creating your own publishing flows.
