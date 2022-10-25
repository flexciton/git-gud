# git-gud
A repository to practice your git skills with. Exercises will be outlined in this Readme, where you can check out various branches and modify them in Git, to show off your skills ;)

This repository has a bunch of protected branches that are in various states. The exercises below use these branches and will ask you to modify them locally so they achieve what the exercise asks for.

## Exercises

### Rewriting your latest commit

This exercise will explore rewriting the commit message of your latest commit on your branch.

<details>
<summary>Exercise</summary>

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
This exercise will explore adding more files to your existing commit.

<details>
<summary>Exercise</summary>

##### Setup
Check out the branch `exercise-latest-commit-add-file`.

Confirm that if you run `git --no-pager diff -r ffd218f HEAD` you see the following:
```bash
git --no-pager diff -r ffd218f HEAD

diff --git a/some_file.txt b/some_file.txt
new file mode 100644
index 0000000..c915c72
--- /dev/null
+++ b/some_file.txt
@@ -0,0 +1 @@
+A file to demonstrate adding to commits.
```
This command shows the changes between the HEAD of your branch and the commit where `exercise-latest-commit-add-file` branched off of (The actual changes is what's important here, not the info at the top).

##### Task
Add to the latest commit so that we include another line in the file:

```bash
git --no-pager diff -r ffd218f HEAD

diff --git a/some_file.txt b/some_file.txt
new file mode 100644
index 0000000..b835cea
--- /dev/null
+++ b/some_file.txt
@@ -0,0 +1,2 @@
+A file to demonstrate adding to commits.
+Changes I've added!
```

</details>

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


