# merge
to merge the main branch into the feature branch:
```bash
git merge feature main
```

this creates a new "merge commit" in the feature branch that ties together histories of both branches, giving a branch structure like:

![merging main into the feature branch](https://wac-cdn.atlassian.com/dam/jcr:4639eeb8-e417-434a-a3f8-a972277fc66a/02%20Merging%20main%20into%20the%20feature%20branh.svg?cdnVersion=1391)

merging is a non-destructive operation, the existing branches are not changed in any way. this also means that the feature branch will have an extraneous merge commit every time we need to incorporate upstream commits.

# rebase
to rebase the feature branch onto main branch:
```bash
git checkout feature
git rebase main
```

this moves the entire `feature` branch to begin on the tip of the `main` branch, effectively incorporating all of the new commits in `main`. instead of using a merge commit, rebasing re-writes the project history by creating brand new commits for each commit in the original branch.

![rebasing the feature branch into main](https://wac-cdn.atlassian.com/dam/jcr:3bafddf5-fd55-4320-9310-3d28f4fca3af/03%20Rebasing%20the%20feature%20branch%20into%20main.svg?cdnVersion=1391)

the major benefit is a much cleaner project history, it eliminates the unnecessary merge commits required by `git merge` and also results in a perfectly linear project history.