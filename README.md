# First exercise

```bash
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git init
Initialized empty Git repository in C:/Users/Samantha/Dropbox/PC/Desktop/The gym/gitHubExercise/.git/
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch 
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
hint: core.useBuiltinFSMonitor=true is deprecated;please set core.fsmonitor=true instead
hint: Disable this message with "git config advice.useCoreFSMonitorConfig false"
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch -m master main
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
hint: core.useBuiltinFSMonitor=true is deprecated;please set core.fsmonitor=true instead
hint: Disable this message with "git config advice.useCoreFSMonitorConfig false"
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status    
hint: core.useBuiltinFSMonitor=true is deprecated;please set core.fsmonitor=true instead
hint: Disable this message with "git config advice.useCoreFSMonitorConfig false"
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git add README.md
hint: core.useBuiltinFSMonitor=true is deprecated;please set core.fsmonitor=true instead
hint: Disable this message with "git config advice.useCoreFSMonitorConfig false"
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git commit -m "first commit"
hint: core.useBuiltinFSMonitor=true is deprecated;please set core.fsmonitor=true instead
hint: Disable this message with "git config advice.useCoreFSMonitorConfig false"
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
hint: core.useBuiltinFSMonitor=true is deprecated;please set core.fsmonitor=true instead
hint: Disable this message with "git config advice.useCoreFSMonitorConfig false"
Switched to branch 'dev'
M       README.md
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git branch -d test
Deleted branch test (was 8211042).
PS C:\Users\Samantha\Dropbox\PC\Desktop\The gym\gitHubExercise> git status
hint: core.useBuiltinFSMonitor=true is deprecated;please set core.fsmonitor=true instead
hint: Disable this message with "git config advice.useCoreFSMonitorConfig false"
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