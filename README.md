# Gym-Git-Exercise-Solutions

## Bundle 1

### exercise 1

```bash
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git init
Initialized empty Git repository in C:/Users/Samantha/Dropbox/PC/Desktop/The gym/gitHubExercise/.git/
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch 
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch -m master main
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status    
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add README.md
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "first commit"
[main (root-commit) 8211042] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch -M main
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git remote add origin https://github.com/Samiskina/gitHubExercises.git
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 232 bytes | 232.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Samiskina/gitHubExercises.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch
  dev
  main
* test
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout dev
Switched to branch 'dev'
M       README.md
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch -d test
Deleted branch test (was 8211042).
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch
* dev
  main
```

###  Exercise 2

```bash
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add home.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git stash
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add about.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git stash
Saved working directory and index state WIP on dev: 9c8c5cd changes
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add team.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git stash
Saved working directory and index state WIP on dev: 9c8c5cd changes
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git stash list
stash@{0}: WIP on dev: 9c8c5cd changes
stash@{1}: WIP on dev: 9c8c5cd changes
stash@{2}: WIP on dev: 9c8c5cd changes
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git stash pop 'stash@{1}'
Rename from 'C:/Users/Samantha/Dropbox/PC/Desktop/The gym/gitHubExercise/.git/index.lock' to 'C:/Users/Samantha/Dropbox/PC/Desktop/The gym/gitHubExercise/.git/index' failed. Should I try again? (y/n) y
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (cbd4bfd5436578ca5c1e9544f774f30f5981762b)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git stash pop 'stash@{1}'
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (4a37c72a998c38d6eba738a4830bc05307e10e07)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add .
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m 'stash'
[dev 6c3d2fa] stash
 2 files changed, 25 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 588 bytes | 588.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Samiskina/gitHubExercises.git
   9c8c5cd..6c3d2fa  dev -> dev
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git stash pop 'stash@{0}'
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{0} (a19810e64b0a5e208a33352507da7c1a07ee6ec8)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git reset --hard
HEAD is now at 6c3d2fa stash
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise>
```

## Bundle 2

### Exercise 1

```bash
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

remote:   https://github.com/Samiskina/GymGitExerciseSolutions.git
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Samiskina/GymGitExerciseSolutions/pull/new/ft/bundle-2
remote:
To https://github.com/Samiskina/gitHubExercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise>
```

### exercise 2

```bash
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout main   
error: Your local changes to the following files would be overwritten by checkout:
        about.html
        home.html
Please commit your changes or stash them before you switch branches.
Aborting
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add .
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch ft/bundle-2
Your branch is up to date with 'origin/ft/bundle-2'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   about.html
        modified:   home.html
        new file:   team.html

PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "feat: added team page"
[ft/bundle-2 d3aaa9a] feat: added team page
 3 files changed, 25 insertions(+), 10 deletions(-)
 create mode 100644 team.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 7 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git pull origin main
From https://github.com/Samiskina/gitHubExercises
 * branch            main       -> FETCH_HEAD
Updating 8211042..4a916ed
Fast-forward
 README.md    | 182 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 about.html   |  12 ++++
 home.html    |  13 +++++
 service.html |  12 ++++
 4 files changed, 218 insertions(+), 1 deletion(-)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add service.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "feat: added h2 and p tag to service page"
[ft/service-redesign 0088b56] feat: added h2 and p tag to service page
 1 file changed, 2 insertions(+)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 354 bytes | 177.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Samiskina/GymGitExerciseSolutions.git
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Samiskina/GymGitExerciseSolutions/pull/new/ft/service-redesign
remote:
To https://github.com/Samiskina/gitHubExercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add service.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "feat: added some changes to service page"
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push
[main 1b68a80] feat: added some changes to service page
 1 file changed, 2 insertions(+)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 374 bytes | 374.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Samiskina/GymGitExerciseSolutions.git
To https://github.com/Samiskina/gitHubExercises.git
   4a916ed..1b68a80  main -> main
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is ahead of 'origin/ft/service-redesign' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git diff origin/main ft/service-redesign
diff --git a/service.html b/service.html
index 27c7b23..48ed8b3 100644
--- a/service.html
+++ b/service.html
@@ -8,7 +8,7 @@
   </head>
   <body>
     <h1>Services we offer</h1>
-    <h2>Working on Bundle 2</h2>
-    <p>doing the exercise 2</p>
+    <h2>Bundle 2</h2>
+    <p>Exercise 2</p>
   </body>
 </html>
```