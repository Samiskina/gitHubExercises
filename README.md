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
```

## Bundle 3

### Exercise 1

```bash

PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add team.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "Feat: added a new team page"
[ft/team-page 8a27cc7] Feat: added a new team page
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 476 bytes | 238.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Samiskina/GymGitExerciseSolutions.git
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Samiskina/GymGitExerciseSolutions/pull/new/ft/team-page
remote:
To https://github.com/Samiskina/gitHubExercises.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add team.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "Feat: added a new team page"
[ft/team-page 8a27cc7] Feat: added a new team page
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 476 bytes | 238.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout  ft/team-page
Switched to branch 'ft/team-page'Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git log
commit 445518365a91d0986cf53390f0d5f1559cd5e27d (HEAD -> ft/team-page, origin/ft/team-page)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout ft/contact-pag
error: pathspec 'ft/contact-pag' did not match any file(s) known to git
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout ft/contact-page
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
On branch ft/team-page
Your branch is up to date with 'origin/ft/team-page'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add README.md
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "Docs: added commands history to README file"
[ft/team-page 9f71309] Docs: added commands history to README file
 1 file changed, 40 insertions(+), 1 deletion(-)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git log
commit 9f71309b8df14f77ee1c4e41024f4640c11f8475 (HEAD -> ft/team-page)
Author: Samiskina <mureraksamantha@gmail.com>
Date:   Wed Oct 12 16:48:16 2022 +0200

    Docs: added commands history to README file

commit 445518365a91d0986cf53390f0d5f1559cd5e27d (origin/ft/team-page)
Author: Samiskina <mureraksamantha@gmail.com>
Date:   Wed Oct 12 16:28:36 2022 +0200

    Docs: updates to the README file

commit 8a27cc7e1345d3b4b2009f49f892f3c74cd5393e
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git checkout ft/contact-page             
Switched to branch 'ft/contact-page'
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git cherry-pick 9f71309b8df14f77ee1c4e41024f4640c11f8475 
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply 9f71309... Docs: added commands history to README file
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add README.md
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "Feat: ft/team-page last commit applied to ft/contact-page" 
[ft/contact-page f310c4d] Feat: ft/team-page last commit applied to ft/contact-page
 Date: Wed Oct 12 16:48:16 2022 +0200
 1 file changed, 71 insertions(+), 1 deletion(-)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git push origin ft/contact-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.03 KiB | 263.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/Samiskina/GymGitExerciseSolutions.git
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Samiskina/GymGitExerciseSolutions/pull/new/ft/contact-page
remote:
To https://github.com/Samiskina/gitHubExercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
```
