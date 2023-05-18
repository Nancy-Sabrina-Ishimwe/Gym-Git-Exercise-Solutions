Git exercises Solutions
#Bundle 1
#Exercise 1
...bash

PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git branch
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git remote
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash
You do not have the initial commit yet
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> 

...

### Exercise 2
...bash
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git status
On branch dev
Untracked files:
        home.html
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git status
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)

PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash
Saved working directory and index state WIP on dev: 8fe8530 first commit
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash list
stash@{0}: WIP on dev: 8fe8530 first commit
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git add about.html
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash list
stash@{1}: WIP on dev: 8fe8530 first commit
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git status        
On branch dev
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git add team.html
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash 
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash list   
stash@{0}: WIP on dev: 8fe8530 first commit
stash@{1}: WIP on dev: 8fe8530 first commit
stash@{2}: WIP on dev: 8fe8530 first commit
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash pop stash@{1}
error: unknown switch `e'
    -q, --quiet           be quiet, only report errors

PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)

Dropped refs/stash@{0} (25fed41ba6015fbd2dfcca76c5080b3ae2e3c7df)
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git add team.html
Saved working directory and index state WIP on dev: 8fe8530 first commit
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git list
git: 'list' is not a git command. See 'git --help'.

The most similar commands are
        bisect
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash list
stash@{0}: WIP on dev: 8fe8530 first commit
stash@{1}: WIP on dev: 8fe8530 first commit
stash@{2}: WIP on dev: 8fe8530 first commit
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash pop stash@{1}
error: unknown switch `e'

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index

PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash pop stash@{1}
error: unknown switch `e'

    -q, --quiet           be quiet, only report errors

PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash pop 'stash@{1}'
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

stash@{0}: WIP on dev: 8fe8530 first commit
stash@{1}: WIP on dev: 8fe8530 first commit
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash pop 'stash@{1}'
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped stash@{1} (6927fa7edb5fb288934880797cc0cbae6cb40f1f)
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git add .
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git commit -m"Exercise 2: Bundle1"
[dev 27293d5] Exercise 2: Bundle1
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 550 bytes | 183.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Nancy-Sabrina-Ishimwe/Gym-Git-Exercise-Solutions.git
   8fe8530..27293d5  dev -> dev
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash list
stash@{0}: WIP on dev: 8fe8530 first commit
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git stash pop 'stash@{0}'
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (da48ec1ea48c5b4c5bf9de95356b4607214e6247)
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> git reset --hard
HEAD is now at 27293d5 Exercise 2: Bundle1
PS C:\Users\Name of Jesus\Desktop\Gym Git Exercise Solutions> 