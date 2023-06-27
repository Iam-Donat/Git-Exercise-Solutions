# Git-Exercises-Solution.

This readme file contain terminal codes solutions to my Git-Exercises 👌 <br> <br>
<img src="./terminal.gif" width="400" style="border-radius: 20px; box-shadow: 2px 2px 2px rgba(31, 130, 125, 0.4)">

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
Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/bundle-2)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 632 bytes | 24.00 KiB/s, done.
From github.com:Iam-Ntwali/Git-Exercises
   cffd8f8..be8d4c8  main       -> origin/main
Updating cffd8f8..be8d4c8
Fast-forward
 about.html    | 14 ++++++++++++++
 home.html     | 14 ++++++++++++++
 services.html | 14 ++++++++++++++
 3 files changed, 42 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ git commit -m "updated services"
[ft/service-redesign dbbb0d0] updated services
 1 file changed, 5 insertions(+)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ push
bash: push: command not found

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 357 bytes | 357.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/ft/service-redesign
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git commit -m "added new changes service page on main"
[main acb083b] added new changes service page on main
 1 file changed, 5 insertions(+)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 364 bytes | 72.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:Iam-Ntwali/Git-Exercises.git
   be8d4c8..acb083b  main -> main

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git switch ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign|MERGING)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign|MERGING)
$ git commit -m "merged changes from services main branch"
[ft/service-redesign 465aec3] merged changes from services main branch

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/service-redesign)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 380 bytes | 380.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:Iam-Ntwali/Git-Exercises.git
   dbbb0d0..465aec3  ft/service-redesign -> ft/service-redesign
```

## Bundle 3

### Exercise 1

```bash
Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git switch -c ft/team-page
Switched to a new branch 'ft/team-page'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/team-page)
$ touch team.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/team-page)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/team-page)
$ git commit -m "created team page"
[ft/team-page 4f9332a] created team page
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 458 bytes | 458.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/ft/team-pag
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/team-page)
$ git log
commit 4f9332a09c0217f77b62ae5aad102f7ffcffd857 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Iam-Ntwali <64748718+Iam-Ntwali@users.noreply.github.com>
Date:   Wed Jun 21 19:07:01 2023 +0200

    created team page

commit acb083bf5dae6ca00e4d69b43fbab749b1487109 (origin/main, main, ft/contact-page)
Author: Iam-Ntwali <64748718+Iam-Ntwali@users.noreply.github.com>
Date:   Wed Jun 21 18:52:01 2023 +0200

    added new changes service page on main

commit be8d4c85fa69f481f5668b35973eb0e86197d0ab
Merge: cffd8f8 ca10312
Author: IYADUKUNZE Emile <80049630+emilenfc@users.noreply.github.com>
Date:   Wed Jun 21 18:06:47 2023 +0200

    Merge pull request #1 from Iam-Ntwali/ft/bundle-2

commit ca103126b34a021b661868f741d172f425e03c43 (origin/ft/bundle-2, ft/bundle-2)
Author: Iam-Ntwali <64748718+Iam-Ntwali@users.noreply.github.com>
Date:   Wed Jun 21 17:43:14 2023 +0200

    services.html

commit cb8aeb3d28db5887bd986743fd40cec240925e98 (origin/dev, dev)
Author: Iam-Ntwali <64748718+Iam-Ntwali@users.noreply.github.com>
Date:   Wed Jun 21 17:28:16 2023 +0200

    added home and about pages

commit cffd8f8d5047ee066d0155f716234fe9bd1ef663
Author: Iam-Ntwali <64748718+Iam-Ntwali@users.noreply.github.com>
Date:   Wed Jun 21 17:13:11 2023 +0200

    initial file

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/contact-page)
$ git cherry-pick 4f9332a09c0217f77b62ae5aad102f7ffcffd857
[ft/contact-page 5601d9e] created team page
 Date: Wed Jun 21 19:07:01 2023 +0200
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/contact-page)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/contact-page)
$ git commit -m "Added Contact Page"
[ft/contact-page 1673b96] Added Contact Page
 1 file changed, 14 insertions(+)
 create mode 100644 contact.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/contact-page)
$ push --set-upstream origin ft/contact-page
bash: push: command not found

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 733 bytes | 733.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/ft/contact-page
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/contact-page)
$ git switch -c ft/faq-page
Switched to a new branch 'ft/faq-page'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ touch faq.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ git commit m- "added new faq page"
error: pathspec 'm-' did not match any file(s) known to git
error: pathspec 'added new faq page' did not match any file(s) known to git

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ git commit -m "added new faq page"
[ft/faq-page 66b40ac] added new faq page
 1 file changed, 14 insertions(+)
 create mode 100644 faq.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 464 bytes | 464.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/ft/faq-page
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ git revert 4f9332a09c0217f77b62ae5aad102f7ffcffd857
[ft/faq-page d79b7b9] Revert "created team page"
 1 file changed, 14 deletions(-)
 delete mode 100644 team.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ git status
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 289 bytes | 289.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:Iam-Ntwali/Git-Exercises.git
   66b40ac..d79b7b9  ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
```
### Exercise 2

```bash

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/faq-page)
$ git checkout -b ft/home-page-redisign
Switched to a new branch 'ft/home-page-redisign'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/home-page-redisign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git statut
git: 'statut' is not a git command. See 'git --help'.

The most similar command is
        status

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    index.html

no changes added to commit (use "git add" and/or "git commit -a")

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git commit -m "deleted unwanted file index.html"
[main aec7fb8] deleted unwanted file index.html
 1 file changed, 14 deletions(-)
 delete mode 100644 index.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 255 bytes | 255.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:Iam-Ntwali/Git-Exercises.git
   acb083b..aec7fb8  main -> main

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git checkout ft/home-page-redesign
error: pathspec 'ft/home-page-redesign' did not match any file(s) known to git

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git checkout ft/home-page-redesign
error: pathspec 'ft/home-page-redesign' did not match any file(s) known to git

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git checkout ft/home-page-redisign
Switched to branch 'ft/home-page-redisign'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/home-page-redisign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redisign.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/home-page-redisign)
$ git status
On branch ft/home-page-redisign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/home-page-redisign)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/home-page-redisign)
$ git commit -m "new changes"
[ft/home-page-redisign de99779] new changes
 1 file changed, 1 insertion(+)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/home-page-redisign)
$ git push
fatal: The current branch ft/home-page-redisign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redisign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/home-page-redisign)
$  git push --set-upstream origin ft/home-page-redisign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.58 KiB | 64.00 KiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redisign' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/ft/home-page-redisign
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      ft/home-page-redisign -> ft/home-page-redisign
branch 'ft/home-page-redisign' set up to track 'origin/ft/home-page-redisign'.

```

## Bundle 4 

### Exercise 1

```bash
Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/home-page-redisign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git remote add git-copy git@github.com:Iam-Ntwali/Git-Exercises-Repo-2.git

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git remote
git-copy
origin

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git commit -m "added some changes"
[main 30ea116] added some changes
 1 file changed, 1 insertion(+)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push origin
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 392 bytes | 392.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:Iam-Ntwali/Git-Exercises.git
   aec7fb8..30ea116  main -> main

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git push git-copy
Enumerating objects: 19, done.
Counting objects: 100% (19/19), done.
Delta compression using up to 4 threads
Compressing objects: 100% (18/18), done.
Writing objects: 100% (19/19), 2.57 KiB | 175.00 KiB/s, done.
Total 19 (delta 8), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (8/8), done.
To github.com:Iam-Ntwali/Git-Exercises-Repo-2.git
 * [new branch]      main -> main
```

### Exercise 2

```bash 
Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/footer)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/footer)
$ git commit -m "added footer page"
[ft/footer 3b15f85] added footer page
 2 files changed, 15 insertions(+)
 create mode 100644 footer.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/footer)
$ git status
On branch ft/footer
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        new page.html

nothing added to commit but untracked files present (use "git add" to track)

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/footer)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/footer)
$ git commit -m "added some random page"
[ft/footer 4ef7d3f] added some random page
 1 file changed, 14 insertions(+)
 create mode 100644 new page.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/footer)
$ git push
fatal: The current branch ft/footer has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/footer

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/footer)
$ git push --set-upstream origin ft/footer
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 842 bytes | 842.00 KiB/s, done.
Total 7 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/ft/footer
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/footer)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/squashing)
$ git merge --squash ft/footer
Updating 30ea116..4ef7d3f
Fast-forward
Squash commit -- not updating HEAD
 footer.html   | 14 ++++++++++++++
 home.html     |  1 +
 new page.html | 14 ++++++++++++++
 3 files changed, 29 insertions(+)
 create mode 100644 footer.html
 create mode 100644 new page.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/squashing)
$ git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   footer.html
        modified:   home.html
        new file:   new page.html


Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/squashing)
$ git commit -m "changes squashed from ft/footer branch"
[ft/squashing b8e07fc] changes squashed from ft/footer branch
 3 files changed, 29 insertions(+)
 create mode 100644 footer.html
 create mode 100644 new page.html

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-exercises (ft/squashing)
$ git push origin ft/squashing
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 660 bytes | 660.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/Iam-Ntwali/Git-Exercises/pull/new/ft/squashing
remote:
To github.com:Iam-Ntwali/Git-Exercises.git
 * [new branch]      ft/squashing -> ft/squashing
```

## Bundle 5

### Exercise 1

```bash
Done the site is live here 👉🏾 https://iam-ntwali.github.io/Git-Exercises/
```

### Exercise 2

```bash
Ntwali@Ntwali-PC MINGW64 ~/Desktop
$ git clone git@github.com:Iam-Ntwali/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 95
Receiving objects: 100% (107/107), 1.95 MiB | 191.00 KiB/s, done.
Resolving deltas: 100% (5/5), done.

Ntwali@Ntwali-PC MINGW64 ~/Desktop
$ cd git-cafe-exercise

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-cafe-exercise (main)
$ code .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-cafe-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .vscode/

no changes added to commit (use "git add" and/or "git commit -a")

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-cafe-exercise (main)
$ git add .

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-cafe-exercise (main)
$ git commit -m "updated index.html"
[main c988951] updated index.html
 2 files changed, 286 insertions(+), 226 deletions(-)
 create mode 100644 .vscode/settings.json

Ntwali@Ntwali-PC MINGW64 ~/Desktop/git-cafe-exercise (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 1.52 KiB | 1.52 MiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:Iam-Ntwali/git-cafe-exercise.git
   d1d3f9c..c988951  main -> main
```
