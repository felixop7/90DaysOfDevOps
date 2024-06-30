# Day 10 Task: Advance Git & GitHub for DevOps Engineers: Part-2

## Git Stash

Git stash is a command that allows you to temporarily save changes you have made in your working directory, without committing them. This is useful when you need to switch to a different branch to work on something else, but you don't want to commit the changes you've made in your current branch yet.

To use Git stash, you first create a new branch and make some changes to it. Then you can use the command `git stash` to save those changes. This will remove the changes from your working directory and record them in a new stash. You can apply these changes later. `git stash list` command shows the list of stashed changes.

You can also use `git stash drop` to delete a stash and `git stash clear` to delete all the stashes.

## Cherry-pick

Git cherry-pick is a command that allows you to select specific commits from one branch and apply them to another. This can be useful when you want to selectively apply changes that were made in one branch to another.

To use `git cherry-pick`, you first create two new branches and make some commits to them. Then you use `git cherry-pick <commit_hash>` command to select the specific commits from one branch and apply them to the other.

## Resolving Conflicts

Conflicts can occur when you merge or rebase branches that have diverged, and you need to manually resolve the conflicts before git can proceed with the merge/rebase. `git status` command shows the files that have conflicts, `git diff` command shows the difference between the conflicting versions and `git add` command is used to add the resolved files.

## Tasks

### Task-01

1. Create a new branch and make some changes to it.
2. Use `git stash` to save the changes without committing them.
3. Switch to a different branch, make some changes and commit them.
4. Use `git stash pop` to bring the changes back and apply them on top of the new commits.

### Task-02

1. In `version01.txt` of the `development` branch add below lines after “This is the bug fix in development branch” that you added in Day10 and reverted to this commit.

   ```
   Line2>> After bug fixing, this is the new feature with minor alteration
   ```

   Commit this with message “Added feature2.1 in development branch”

   ```
   Line3>> This is the advancement of previous feature
   ```

   Commit this with message “Added feature2.2 in development branch”

   ```
   Line4>> Feature 2 is completed and ready for release
   ```

   Commit this with message “Feature2 completed”

2. All these commit messages should be reflected in the `Production` branch too which will come out from the `Master` branch (Hint: try rebase).

### Task-03

1. In the `Production` branch Cherry pick Commit “Added feature2.2 in development branch” and add below lines in it:

   ```
   Line to be added after Line3>> This is the advancement of previous feature
   Line4>> Added few more changes to make it more optimized.
   ```

   Commit: Optimized the feature

## Solution Steps

### Task-01 Solution Steps

1. Create and switch to a new branch:
   ```bash
   git checkout -b new-branch
   ```
2. Make some changes to a file, e.g., `version01.txt`.
3. Stash the changes:
   ```bash
   git stash
   ```
4. Switch to a different branch:
   ```bash
   git checkout different-branch
   ```
5. Make some changes and commit them:
   ```bash
   git add .
   git commit -m "Made changes in different-branch"
   ```
6. Pop the stashed changes back:
   ```bash
   git stash pop
   ```

### Task-02 Solution Steps

1. Switch to the `development` branch:
   ```bash
   git checkout development
   ```
2. Edit `version01.txt` to add the specified lines.
3. Commit each change with the specified messages:

   ```bash
   echo "After bug fixing, this is the new feature with minor alteration" >> version01.txt
   git add version01.txt
   git commit -m "Added feature2.1 in development branch"

   echo "This is the advancement of previous feature" >> version01.txt
   git add version01.txt
   git commit -m "Added feature2.2 in development branch"

   echo "Feature 2 is completed and ready for release" >> version01.txt
   git add version01.txt
   git commit -m "Feature2 completed"
   ```

4. Rebase the commits onto the `Production` branch:
   ```bash
   git checkout production
   git rebase development
   ```

### Task-03 Solution Steps

1. Switch to the `Production` branch:
   ```bash
   git checkout production
   ```
2. Cherry-pick the specific commit:
   ```bash
   git cherry-pick <commit_hash_of_feature2.2>
   ```
3. Edit `version01.txt` to add the specified lines:
   ```bash
   echo "Added few more changes to make it more optimized." >> version01.txt
   git add version01.txt
   git commit --amend -m "Optimized the feature"
   ```

## Summary

In this session, we learned about advanced Git commands like `git stash`, `git cherry-pick`, and how to resolve conflicts. We also practiced these commands through tasks that involved stashing changes, rebasing commits, and cherry-picking specific commits.

## References

- [Complete Git and GitHub Tutorial](https://www.youtube.com/watch?v=apGV9Kg7ics).

---

Happy Coding! 🚀

**Roshan Sahani**
