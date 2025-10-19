---
{"dg-publish":true,"permalink":"/3-resources/technical/trunk-based-development/","tags":["🌲_Evergreen","☢️_Atomic","🔧_Technical"],"updated":"2025-10-19T07:46:53.174-07:00"}
---


### Trunk-Based Development

Trunk-Based Development was popularized in the `svn` and `perforce` days. It's very similar to the GitHub Flow based development, except that unfinished work is gated behind a feature flag. The focus of this method is that all changes should be small, incremental changes. You should aim to merge into main as often as possible, multiple times a day if possible.

#### Workflow
1. Create a branch off of `main` for a new small piece of work.
2. (maybe) Add a feature flag to your FF system (e.g. LaunchDarkly).
3. Commit changes to this new branch.
4. PR to merge into main.
5. Merge into main.
6. CI automatically deploys to staging.
7. (maybe) Turn feature flag on in staging.
8. Test in staging.
9. When ready, run CI action to deploy to production.
#### Pros
1. Continuous Integration of new code.
2. Very simple.
3. Merging often and in small increments mitigates merge conflict overhead.

#### Cons
1. Adequate automated testing is assumed in this process.
2. Needs a feature flag system for anything non-trivial.
3. PR process might be too slow. Best if you do Pair/Mob programming to avoid external code review.