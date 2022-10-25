# git-gud
A repository to practice your git skills with. Exercises will be outlined in this Readme, where you can check out various branches and modify them in Git, to show off your skills ;)

This repository has a bunch of protected branches that are in various states. The exercises below use these branches and will ask you to modify them locally so they achieve what the exercise asks for.

## Exercises

### Rewriting your latest commit

This exercise will explore renaming your latest commit on your branch.

<details>
<summary>Setup</summary>

##### Setup
Check out the branch `exercise-latest-commit-rewrite`.

Confirm that if you run `git --no-pager log --pretty=format:%s 81795d5..HEAD` you see the following:
```bash
git --no-pager log --pretty=format:%s 81795d5..HEAD
CHANGE ME
```
This command shows the commit messages between the HEAD of your branch and the commit where `exercise-latest-commit-rewrite` branched off of (if there is a % that can be ignored).

##### Task
Change the message of the latest commit so that it instead displays the following:

```bash
git --no-pager log --pretty=format:%s 81795d5..HEAD
changed%
```

</details>


### Adding to your latest commit

### Rebasing

### Rebasing with conflict

### Rewriting an earlier commit on your branch

### Adding to an earlier commit on your branch

### Combining sequential commits

#### Squash

#### Fixup

### Reordering commits

### Combining non-sequential commits

### Splitting a commit in two


