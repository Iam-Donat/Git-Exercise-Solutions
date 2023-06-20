# Git-Exercises-Solution.

This repo contain solutions to Git-Exercises 👌
<img src="./terminal.gif">

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
$ code .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        terminal.gif

nothing added to commit but untracked files present (use "git add" to track)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   terminal.gif


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git commit -m "initial commit"
[main (root-commit) 54018b6] initial commit
 2 files changed, 18 insertions(+)
 create mode 100644 README.md
 create mode 100644 terminal.gif

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git remote add origin git@github.com:Iam-Ntwali/Git-Exercise-Solutions.git

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push --set-upstream origin main
To github.com:Iam-Ntwali/Git-Exercise-Solutions.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:Iam-Ntwali/Git-Exercise-Solutions.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git fetch
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 620 bytes | 6.00 KiB/s, done.
From github.com:Iam-Ntwali/Git-Exercise-Solutions
 * [new branch]      main       -> origin/main

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git status
On branch main
nothing to commit, working tree clean

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git merge
fatal: No remote for the current branch.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push --set-upstream origin main
To github.com:Iam-Ntwali/Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:Iam-Ntwali/Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git branch --set-upstream-to=origin/main main
branch 'main' set up to track 'origin/main'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push
To github.com:Iam-Ntwali/Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:Iam-Ntwali/Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git pull remote main
fatal: 'remote' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git help push

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push --all
To github.com:Iam-Ntwali/Git-Exercise-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:Iam-Ntwali/Git-Exercise-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push -f
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 101.91 KiB | 328.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:Iam-Ntwali/Git-Exercise-Solutions.git
 + 2cc72bc...54018b6 main -> main (forced update)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git branch dev

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git switch dev
Switched to branch 'dev'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git branch test

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git switch test
Switched to branch 'test'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (test)
$ git switch dev
Switched to branch 'dev'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git branch -d test
Deleted branch test (was 54018b6).

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercise-Solutions/pull/new/dev
remote:
To github.com:Iam-Ntwali/Git-Exercise-Solutions.git
 * [new branch]      dev -> dev

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (dev)
$
```

### Exercise 2

```bash

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git add home.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash
Saved working directory and index state WIP on main: 50e3b22 initial commit

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ touch about.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git add about.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash
Saved working directory and index state WIP on main: 50e3b22 initial commit

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ touch team.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git add team.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash
Saved working directory and index state WIP on main: 50e3b22 initial commit

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: WIP on main: 50e3b22 initial commit
stash@{1}: WIP on main: 50e3b22 initial commit
stash@{2}: WIP on main: 50e3b22 initial commit

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash pop stash{1}
error: stash{1} is not a valid reference

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (252b917f2733944380de9172029db90961a9bf90)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: WIP on main: 50e3b22 initial commit
stash@{1}: WIP on main: 50e3b22 initial commit

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (071fbc9e0477b39a3e0f550fbb4a9dac8715e6e9)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git commit -m "added about and home pages"
[main 48b77ce] added about and home pages
 2 files changed, 28 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 598 bytes | 598.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:Iam-Ntwali/Git-Exercise-Solutions.git
   50e3b22..48b77ce  main -> main

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: WIP on main: 50e3b22 initial commit

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (b2294ef53d888fe13d810d6990bde2536d041f35)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git reset --hard
HEAD is now at 48b77ce added about and home pages

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$
```

## Bundle 2

### Exercise 1

```bash

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (main)
$ git switch -c ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (ft/bundle-2)
$ touch services.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

no changes added to commit (use "git add" and/or "git commit -a")

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (ft/bundle-2)
$ git add sercives.html
fatal: pathspec 'sercives.html' did not match any files

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (ft/bundle-2)
$ git add services.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (ft/bundle-2)
$ git commit -m "added service page"
[ft/bundle-2 bf03435] added service page
 1 file changed, 14 insertions(+)
 create mode 100644 services.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (ft/bundle-2)
$  git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 470 bytes | 470.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To github.com:Iam-Ntwali/Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/Git-Exercise-Solutions (ft/bundle-2)
$
```
