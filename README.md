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
```commandline
git --no-pager log --pretty=format:%s 81795d5..HEAD

CHANGE ME
```
This command shows the commit messages between the HEAD of your branch and the commit where `exercise-latest-commit-rewrite` branched off of (if there is a % that can be ignored).

##### Task
Change the message of the latest commit so that it instead displays the following:

```commandline
git --no-pager log --pretty=format:%s 81795d5..HEAD

changed%
```

</details>

### Adding to your latest commit
This exercise will explore adding more content to your existing commit. This is very handy if you have already made a commit but forgot to include something that you subsequently need to add.

<details>
<summary>Exercise</summary>

##### Setup
Check out the branch `exercise-latest-commit-add-file`.

Confirm that if you run `git --no-pager diff -r ffd218f HEAD` you see the following:
```commandline
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

```commandline
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
This exercise will explore rebasing. Rebasing is very nice as it allows us to have a clean commit history, and avoids messy merges. Doing a basic rebase is also the building block of doing more interesting techniques, such as the interactive rebase, which is where all the magic happens.

<details>
<summary>Exercise</summary>

##### Setup

In this exercise we'll be playing with two branches. The first one is `exercise-rebasing-base`. Pretend to see this one as the 'main' branch in your repo. This is typically the branch you want to merge your work into eventually. The other branch we will be using is `exercise-rebasing-rebase-branch`. Pretend this is your 'feature' branch that you've been doing development on.

The key thing to notice here is that work has been happening on our base branch after we branched off with our feature branch. If you do `git log origin/exercise-rebasing-rebase-branch` you can see that there is a commit to 'add sample file 2', however you can't see the 'add sample file 1' commit. This is because we branched off of the base branch before this commit happened (we branched off at b9dd7a0). If you do `git log origin/exercise-rebasing-base` you can see that we've added the 'add sample file 1' commit after where we branched off.

Check out the branch `exercise-rebasing-rebase-branch` and run `git --no-pager log --pretty=format:%s b9dd7a0..HEAD` to confirm you can only see the 'add sample file 2' commit:

```commandline
git --no-pager log --pretty=format:%s b9dd7a0..HEAD

add sample file 2 (should be applied after sample file 1)
```

##### Task
Rebase `exercise-rebasing-rebase-branch` onto `exercise-rebasing-base` so that the 'feature' branch will have its commits on top of the 'base' branch. Output should look like this:

```commandline
git --no-pager log --pretty=format:%s b9dd7a0..HEAD

add sample file 2 (should be applied after sample file 1)
add sample file 1 (should be applied before sample file 2)
```

If you do a simple `git log` you should now see that the base of your feature branch is again on top of the base branch, with your extra commit adding file 2.

</details>

### Rebasing with conflict

### Rewriting an earlier commit on your branch

### Adding to an earlier commit on your branch

### Combining sequential commits

#### Squash

#### Fixup

### Reordering commits

### Combining non-sequential commits

### Splitting a commit in two


