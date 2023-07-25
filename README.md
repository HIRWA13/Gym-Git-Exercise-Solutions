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