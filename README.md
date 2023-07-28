# Git Exercises


## Git Bundle 1


### Exercise 1

```bash

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises
$ git init
Initialized empty Git repository in C:/Users/User/projects/GitExercises/.git/

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (master)
$ git branch -M main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ touch index.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
index.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ touch style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
index.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        style.css

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git add --all

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git commit -m "git Exercise 1"
[main (root-commit) 72e29c0] git Exercise 1
 2 files changed, 21 insertions(+)
 create mode 100644 index.html
 create mode 100644 style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git remote add origin https://github.com/HIRWA13/Git-Exercises.git

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 432 bytes | 432.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/HIRWA13/Git-Exercises.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git branch dev

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout dev
Switched to branch 'dev'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (dev)
$ git branch test

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (dev)
$ git branch
* dev
  main
  test

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (dev)
$ igt checkout test
bash: igt: command not found

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (dev)
$ git checkout test
Switched to branch 'test'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (test)
$ git checkout dev
Switched to branch 'dev'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (dev)
$ git branch -d test
Deleted branch test (was 72e29c0).

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (dev)
$ git branch
* dev
  main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (dev)

```




### Exercise 2

## what is git stash?

git stash is a command that allows you to save changes that you don't want to commit immediately. It takes the dirty state of your working directory — that is, your modified tracked files and staged changes — and saves it on a stack of unfinished changes that you can reapply at any time.

```bash

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ touch home.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
home.html  index.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git add --all

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash
Saved working directory and index state WIP on main: 72e29c0 git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ touch about.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git add --all

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash
Saved working directory and index state WIP on main: 72e29c0 git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ touch team.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git add --all

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash
Saved working directory and index state WIP on main: 72e29c0 git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
index.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash list
stash@{0}: WIP on main: 72e29c0 git Exercise 1
stash@{1}: WIP on main: 72e29c0 git Exercise 1
stash@{2}: WIP on main: 72e29c0 git Exercise 1
stash@{3}: WIP on dev: 72e29c0 git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (e14ff0e240971cb6c90a28d48b696a14badfba98)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
about.html  index.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash list
stash@{0}: WIP on main: 72e29c0 git Exercise 1
stash@{1}: WIP on main: 72e29c0 git Exercise 1
stash@{2}: WIP on dev: 72e29c0 git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (958808d97b482cb8dfa029e24ebbf04416d911fb)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git commit -m "added home.html and about.html"
[main 900648a] added home.html and about.html
 2 files changed, 34 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 649 bytes | 649.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/HIRWA13/Git-Exercises.git
   72e29c0..900648a  main -> main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash list
stash@{0}: WIP on main: 72e29c0 git Exercise 1
stash@{1}: WIP on dev: 72e29c0 git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git shash pop stash@{0}
git: 'shash' is not a git command. See 'git --help'.

The most similar command is
        stash

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (dc007cfed87ba60c3f0ba0788917bbbace5a00ba)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
about.html  home.html  index.html  style.css  team.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git reset --hard
HEAD is now at 900648a added home.html and about.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)


```





## Git Bundle 2


### Exercise 1

```bash

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git branch ft/bundle-2

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
about.html  home.html  index.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ touch services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ touch services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git add services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   services.html


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git commit -m "added the services.html page"
[ft/bundle-2 3f35f55] added the services.html page
 1 file changed, 10 insertions(+)
 create mode 100644 services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git push -u ft/bundle-2
fatal: 'ft/bundle-2' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ ^C

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ ^[[200~git push --set-upstream origin ft/bundle-2
bash: $'\E[200~git': command not found

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 402 bytes | 402.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/HIRWA13/Git-Exercises/pull/new/ft/bundle-2
remote:
To https://github.com/HIRWA13/Git-Exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)

```


### Exercise 2

<b>git diff:</b> git diff command is used to show the changes between the working tree and the index or a tree, changes between the index and a tree, changes between two trees, changes between one branch and another branch.

```bash

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git branch ft/service-redesign

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
about.html  home.html  index.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/bundle
error: pathspec 'ft/bundle' did not match any file(s) known to git

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'
Your branch is up to date with 'origin/ft/bundle-2'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ ls
about.html  home.html  index.html  services.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git merge ft/bundle-2
Updating 900648a..3f35f55
Fast-forward
 services.html | 10 ++++++++++
 1 file changed, 10 insertions(+)
 create mode 100644 services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
about.html  home.html  index.html  services.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ ls
about.html  home.html  index.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git merge main
Updating 900648a..3f35f55
Fast-forward
 services.html | 10 ++++++++++
 1 file changed, 10 insertions(+)
 create mode 100644 services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ ls
about.html  home.html  index.html  services.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git add sercices.html
fatal: pathspec 'sercices.html' did not match any files

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git add services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git commit -m "modified the services.html page"
[ft/service-redesign 8bad055] modified the services.html page
 1 file changed, 2 insertions(+), 2 deletions(-)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git push -u ft/service-redisigned
fatal: 'ft/service-redisigned' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git push -u origin ft/service-redisigned
error: src refspec ft/service-redisigned does not match any
error: failed to push some refs to 'https://github.com/HIRWA13/Git-Exercises.git
'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ ^C

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 12 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (14/14), 1.55 KiB | 794.00 KiB/s, done.
Total 14 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), done.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/HIRWA13/Git-Exercises/pull/new/ft/service-redesi
gn
remote:
To https://github.com/HIRWA13/Git-Exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git commit -m "changes to the services.html"
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git add services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git commit -m "changes to the services.html"
[main 35dd828] changes to the services.html
 1 file changed, 2 insertions(+), 2 deletions(-)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git push
To https://github.com/HIRWA13/Git-Exercises.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/HIRWA13/Git-Exercises.git
'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 644 bytes | 128.00 KiB/s, done.
From https://github.com/HIRWA13/Git-Exercises
   900648a..bd7250b  main       -> origin/main
Merge made by the 'ort' strategy.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git push
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 522 bytes | 522.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/HIRWA13/Git-Exercises.git
   bd7250b..88b2400  main -> main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git diff

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git diff main
diff --git a/services.html b/services.html
index a66d9e8..9885513 100644
--- a/services.html
+++ b/services.html
@@ -4,7 +4,7 @@
 <link rel="stylesheet" href="style.css">
 </head>
 </body>
-<h1>Welcome to Our Services Page which is cool</h1>
-<p>secret servicesssss</p>
+<h1>Welcome to Our Services Page and it is awesome</h1>
+<p>We have a variety of services including: plumbing, shoping and many more...!
</p>
 </body>
 </html>
\ No newline at end of file

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git merge ft/service-redesign
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main|MERGING)
$ git add service.html
fatal: pathspec 'service.html' did not match any files

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main|MERGING)
$ ls
about.html  home.html  index.html  services.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main|MERGING)
$ git add services.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main|MERGING)
$ git commit -m "resolved the conflicts"
[main eff90ca] resolved the conflicts

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 350 bytes | 350.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/HIRWA13/Git-Exercises.git
   88b2400..eff90ca  main -> main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$

```

## Git Bundle 3


### Exercise 1

```bash

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ ls
about.html  home.html  index.html  services.html  style.css

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ touch team.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git add .

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git commit -m "added the team page"
[ft/team-page ee801c8] added the team page
 1 file changed, 10 insertions(+)
 create mode 100644 team.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ ^C

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ ^[[200~git push --set-upstream origin ft/team-page
bash: $'\E[200~git': command not found

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 410 bytes | 410.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/HIRWA13/Git-Exercises/pull/new/ft/team-page
remote:
To https://github.com/HIRWA13/Git-Exercises.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git log --oneline
ee801c8 (HEAD -> ft/team-page, origin/ft/team-page) added the team page
eff90ca (origin/main, main, ft/contact-page) resolved the conflicts
88b2400 Merge branch 'main' of https://github.com/HIRWA13/Git-Exercises
35dd828 changes to the services.html
8bad055 (origin/ft/service-redesign, ft/service-redesign) modified the services.html page
bd7250b Merge pull request #1 from HIRWA13/ft/bundle-2
3f35f55 (origin/ft/bundle-2, ft/bundle-2) added the services.html page
900648a added home.html and about.html
72e29c0 (dev) git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ ^C

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git log --oneline
ee801c8 (HEAD -> ft/team-page, origin/ft/team-page) added the team page
eff90ca (origin/main, main, ft/contact-page) resolved the conflicts
88b2400 Merge branch 'main' of https://github.com/HIRWA13/Git-Exercises
35dd828 changes to the services.html
8bad055 (origin/ft/service-redesign, ft/service-redesign) modified the services.html page
bd7250b Merge pull request #1 from HIRWA13/ft/bundle-2
3f35f55 (origin/ft/bundle-2, ft/bundle-2) added the services.html page
900648a added home.html and about.html
72e29c0 (dev) git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git cherry-pick ee801c8
[ft/contact-page f8d755b] added the team page
 Date: Fri Jul 28 16:04:50 2023 +0200
 1 file changed, 10 insertions(+)
 create mode 100644 team.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git log --oneline
f8d755b (HEAD -> ft/contact-page) added the team page
eff90ca (origin/main, main) resolved the conflicts
88b2400 Merge branch 'main' of https://github.com/HIRWA13/Git-Exercises
35dd828 changes to the services.html
8bad055 (origin/ft/service-redesign, ft/service-redesign) modified the services.html page
bd7250b Merge pull request #1 from HIRWA13/ft/bundle-2
3f35f55 (origin/ft/bundle-2, ft/bundle-2) added the services.html page
900648a added home.html and about.html
72e29c0 (dev) git Exercise 1

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ touch contact.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git status
On branch ft/contact-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        contact.html

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git add --all

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git commit -m "added the contact us page"
[ft/contact-page a04e25a] added the contact us page
 1 file changed, 10 insertions(+)
 create mode 100644 contact.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ ^C

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$  git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 775 bytes | 775.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/HIRWA13/Git-Exercises/pull/new/ft/contact-page
remote:
To https://github.com/HIRWA13/Git-Exercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git branch
  dev
  ft/bundle-2
* ft/contact-page
  ft/service-redesign
  ft/team-page
  main

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ touch faq.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git status
On branch ft/faq-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git add .

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git commit -m "added the faq page"
[ft/faq-page 8c75e15] added the faq page
 1 file changed, 10 insertions(+)
 create mode 100644 faq.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git push --set-ipstream origin ft/faq-page
error: unknown option `set-ipstream'
usage: git push [<options>] [<repository> [<refspec>...]]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --repo <repository>   repository
    --all                 push all branches
    --branches            alias of --all
    --mirror              mirror all refs
    -d, --delete          delete refs
    --tags                push tags (can't be used with --all or --branches or --mirror)
    -n, --dry-run         dry run
    --porcelain           machine-readable output
    -f, --force           force updates
    --force-with-lease[=<refname>:<expect>]
                          require old value of ref to be at this value
    --force-if-includes   require remote updates to be integrated locally
    --recurse-submodules (check|on-demand|no)
                          control recursive pushing of submodules
    --thin                use thin pack
    --receive-pack <receive-pack>
                          receive pack program
    --exec <receive-pack>
                          receive pack program
    -u, --set-upstream    set upstream for git pull/status
    --progress            force progress reporting
    --prune               prune locally removed refs
    --no-verify           bypass pre-push hook
    --follow-tags         push missing but relevant tags
    --signed[=(yes|no|if-asked)]
                          GPG sign the push
    --atomic              request atomic transaction on remote side
    -o, --push-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only


User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ ^C

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 406 bytes | 406.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/HIRWA13/Git-Exercises/pull/new/ft/faq-page
remote:
To https://github.com/HIRWA13/Git-Exercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.



[ft/faq-page f7fa169] Revert "added the team page"
 1 file changed, 10 deletions(-)
 delete mode 100644 team.html

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git add --all

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git commit -m "reverted the changes from team-page commit"
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 279 bytes | 279.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/HIRWA13/Git-Exercises.git
   8c75e15..f7fa169  ft/faq-page -> ft/faq-page

User@DESKTOP-72SEU4G MINGW64 ~/projects/GitExercises (ft/faq-page)
$
```