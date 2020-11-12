# npm publish

## Step 3 - Publishing in a Monorepo

Knowing how to publish from a monorepo is an important extra step. Monorepos present extra interesting challenges to publishing:

1. Logistically, going in to each package and running a build script and then a publish script is very inefficient
2. You may not want to publish every package every time, meaning going in to each package to publish can lead to errors
3. There may be inter-dependencies between packages, and publishing one may mean you should also publish a second, but you may want to update the dependency of the second package. (this sentence is too dense  ?? fix it? )
4. Some packages are private, and you need to understand how to ensure these private packages are NOT published - ?? could this be its own step? 

Luckily, Thinkmill and Atlassian have developed a tool that helps manage this complexity - [changesets](https://github.com/atlassian/changesets).

Work inside the directory `/simple-monorepo` or copy the directory's contents to a new project. 

Set up changesets for the monorepo.

Edit the package.json script "release" to provide a way to publish all of the packages at once. 

Only publish packages that have changes made. 

## Bonus

- Add preconstruct and manypkg to your monorepo  ?? explain why? 
