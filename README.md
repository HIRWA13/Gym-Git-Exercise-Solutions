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