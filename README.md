# Git-Exercises-Solution.

This readme file contain terminal codes solutions to my Git-Exercises 👌 <br> <br>
<img src="./terminal.gif" width="400" style="border-radius: 10px">

## Bundle 1

### Exercise 1

```bash
Ntwali@Ntwali-PC MINGW64 ~/Desktop
$ mkdir git-exercises

Ntwali@Ntwali-PC MINGW64 ~/Desktop
$ cd git-exercises

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises
$ git init
Initialized empty Git repository in C:/Users/Ntwali/Desktop/git-exercises/.git/

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git branch -M master

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (master)
$ git branch -M main

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ touch home.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ code .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git commit -m "initial commit"
[main (root-commit) 03c700c] initial commit
 1 file changed, 14 insertions(+)
 create mode 100644 home.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git remote add origin git@github.com:Iam-Ntwali/Git-Exercises.git

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git branch -M main

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 409 bytes | 409.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git checkout -b dev
Switched to a new branch 'dev'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/dev
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      dev -> dev

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git checkout -b test
Switched to a new branch 'test'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/test
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      test -> test
 
Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (test)
$ git switch dev
Switched to branch 'dev'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git branch -d test
Deleted branch test (was 03c700c).

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git push origin --delete test
To github.com:Iam-Ntwali/Git-Exercises.git
 - [deleted]         test
```

### Exercise 2

```bash
Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git status
On branch dev
nothing to commit, working tree clean

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ touch home.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git add home.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: cffd8f8 initial file

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ touch about.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git add about.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: cffd8f8 initial file

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: cffd8f8 initial file
stash@{1}: WIP on dev: cffd8f8 initial file

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ touch team.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git add team.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git stash
Saved working directory and index state WIP on dev: cffd8f8 initial file

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git stash list
stash@{0}: WIP on dev: cffd8f8 initial file
stash@{1}: WIP on dev: cffd8f8 initial file
stash@{2}: WIP on dev: cffd8f8 initial file

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (c1daececd999ca5e5f27ca9338bc618801f8a8e0)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (0633282c2471946b81cba99a387ca4bb9bb62f82)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git commit -m "added home and about pages"
[dev cb8aeb3] added home and about pages
 2 files changed, 28 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 555 bytes | 277.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:Iam-Ntwali/Git-Exercises.git
   cffd8f8..cb8aeb3  dev -> dev

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$  git push --set-upstream origin dev
Everything up-to-date
branch 'dev' set up to track 'origin/dev'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (fb60fbb7308640f895f6ff19fcba8e7b77f9f57d)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git reset --hard
HEAD is now at cb8aeb3 added home and about pages
```

## Bundle 2

### Exercise 1

```bash
Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/bundle-2)
$ git status
On branch ft/bundle-2
nothing to commit, working tree clean

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/bundle-2)
$ touch services.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/bundle-2)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/bundle-2)
$ git commit -m "services.html"
[ft/bundle-2 ca10312] services.html
 1 file changed, 14 insertions(+)
 create mode 100644 services.html

 Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/bundle-2)
$  git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 462 bytes | 462.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/ft/bundle-2
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```

### Exercise 2

```bash

```

## Bundle 3

### Exercise 1

```bash

```
