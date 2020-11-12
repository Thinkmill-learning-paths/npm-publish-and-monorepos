# npm publish

## Step 4 - Automate your Publishing

By now, you should have a process/workflow you can run to publish your packages, however it likely involves several manual steps. We want to change that.

For this process, we want to take our `simple-monorepo` have a documented workflow on how contributors:

- Design a workflow for deployment - what actions are automated, and what actions users/publishers need to take - discuss this with Noviny. The assumptions are:
  - There will be many contributors
  - Contributors need to be safe-guarded against failing to release their code - ??what does this mean
  - There is a single 'decider' on when to publish - ??what does this mean
  - The publisher should run as few commands as possible - ??is the publisher not just running `yarn release`
- After discussing it, implement it in a clone of the simple monorepo

TM has prior art on this here:

- [action](https://github.com/changesets/action) - ??briefly explain what this is
- [bot](https://github.com/changesets/bot) - ??briefly explain what this is

