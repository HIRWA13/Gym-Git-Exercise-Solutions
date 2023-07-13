# Gym-Git-Exercise-Solutions

## Bundle 1 Exercise 1

PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> ls

    Directory: C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1

Mode LastWriteTime Length Name

---

-a--- 13-Jul-23 11:58 AM 258 index.html
-a--- 13-Jul-23 11:55 AM 0 README.md

PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git init
Reinitialized existing Git repository in C:/Users/VENZS/Desktop/DESKTOP/gitexercises/exercise1/.git/
PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git branch -M main  
PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git branch

- main
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git add --all
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git commit -m "a new about html file"
  [main bb8a3f5] a new about html file
  1 file changed, 11 insertions(+)
  create mode 100644 about.html
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git push
  Enumerating objects: 9, done.
  Counting objects: 100% (9/9), done.
  Delta compression using up to 2 threads
  Compressing objects: 100% (6/6), done.
  Writing objects: 100% (7/7), 795 bytes | 113.00 KiB/s, done.
  Total 7 (delta 1), reused 0 (delta 0), pack-reused 0
  remote: Resolving deltas: 100% (1/1), done.
  remote: This repository moved. Please use the new location:
  remote: https://github.com/HIRWA13/Gym-Git-Exercise-Solutions.git
  To https://github.com/HIRWA13/Gym-Git-Exercises.git
  5499efe..bb8a3f5 main -> main
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git add --all
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git commit -m "removed the old readme file"
  [main ad00d99] removed the old readme file
  1 file changed, 0 insertions(+), 0 deletions(-)
  delete mode 100644 README.md
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git push
  Enumerating objects: 3, done.
  Counting objects: 100% (3/3), done.
  Delta compression using up to 2 threads
  Compressing objects: 100% (2/2), done.
  Writing objects: 100% (2/2), 274 bytes | 91.00 KiB/s, done.
  Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
  remote: This repository moved. Please use the new location:
  remote: https://github.com/HIRWA13/Gym-Git-Exercise-Solutions.git
  To https://github.com/HIRWA13/Gym-Git-Exercises.git
  bb8a3f5..ad00d99 main -> main
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git pull
  remote: Enumerating objects: 4, done.
  remote: Counting objects: 100% (4/4), done.
  remote: Compressing objects: 100% (3/3), done.
  remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  Unpacking objects: 100% (3/3), 731 bytes | 2.00 KiB/s, done.
  From https://github.com/HIRWA13/Gym-Git-Exercises
  ad00d99..57ba5ed main -> origin/main
  Updating ad00d99..57ba5ed
  Fast-forward
  README.md | 2 ++
  1 file changed, 2 insertions(+)
  create mode 100644 README.md
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git branch dev  
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git branch
  dev
- main
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git checkout dev
  Switched to branch 'dev'
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git branch test
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git branch
- dev
  main
  test
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git branch -d test  
  Deleted branch test (was 57ba5ed).
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git branch
- dev
  main
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git add --all
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git commit -m "created a new branch dev and from it I created another branch test but had to delete it too later "
  On branch dev
  nothing to commit, working tree clean
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git status
  On branch dev
  nothing to commit, working tree clean
  PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git status
  On branch dev
  Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  modified: about.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git add --all
PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git commit -m "created a new branch dev and from it I created another branch test but had to delete it too later "
[dev cffeeb4] created a new branch dev and from it I created another branch test but had to delete it too later
1 file changed, 5 insertions(+)
PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\VENZS\Desktop\DESKTOP\gitexercises\exercise1> git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 626 bytes | 104.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: This repository moved. Please use the new location:
remote: https://github.com/HIRWA13/Gym-Git-Exercise-Solutions.git
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote: https://github.com/HIRWA13/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/HIRWA13/Gym-Git-Exercises.git

- [new branch] dev -> dev
  branch 'dev' set up to track 'origin/dev'.

## Bundle 1 Exercise 2
