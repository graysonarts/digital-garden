---
{"dg-publish":true,"permalink":"/3-resources/git-hub-flow/","tags":["DevWorkflow","🌲_Evergreen","🗒️_Note","🔧_Technical"],"updated":"2025-10-19T07:50:48.845-07:00"}
---

# GitHubFlow

GitHubFlow is a simplified version of [GitFlow](TODO) which eliminates alot of the complexity and overhead for smaller teams.

## Workflow
1. Create a branch off of `main` for a new piece of work
2. Commit to this new branch
3. Push regularly to GitHub for CI testing
4. Before PR, rebase (or merge) main into feature branch
5. Use PR for feedback.
6. Merge into `main` (best to use squash-commits to make it easier to roll back)
7. CI automatically deploys to `staging`
8. When ready to deploy to production, run manual CI GitHub Action
## Requirements for this strategy to work.
### 1. Anything in main is shippable.
This is the main rule that has to be maintained in order. Because anyone, at any time, can deploy to production, if we don't have a high enough quality, it's easy to ship broken code.

### 2. All merges into `main` must go through PR.
This plays off of #1. Everything needs to be reviewed before it makes it to main so avoid human error. GitHub's branch protection should be used to ensure this.

## Pros
1. Simple to understand, and basically built into GitHub through the normal strategy.
2. Minimal overhead of managing the process once GitHub actions (or other CI) are in place.

## Cons
1. Adequate automated testing is assumed in this process.
2. Human error is possible in the deployment process.
3. Merge conflicts in your feature branch have some overhead.
4. Requires discipline to have small PRs and that the code is shippable before PR is merged.