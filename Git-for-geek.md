### Basics of Git
```

git help config
git config --global user.name 'Dibyendu'
git init ( Initialize an empty repository )
git add *.txt
git status ( See your status )
git commit -m "Commit Messages" ( Make a commit to files which are in staging area)
git log ( to see the commit history)

```
### Adding files for staging
```

git add . ( Adds everything )
git add a.txt b.txt ( add files selectively )
git add --all ( Add all files )
git add \*.txt ( Add all *.txt files in current Diretory) 
git add docs/*.txt ( Add all the *.txt files in the docs dirctory
git add "*.txt" Add all *.txt files in the whole project

```
### Staging
```

git diff ( Show unstaged difference since last commit)
git add *.txt
git diff ( No difference after files are staged )
git diff --staged ( View staged difference)
git reset HEAD Somefile ( To remove from a staged area ; HEAD refers to last commit on the timeline)
git checkout -- FileName ( reomove all the changes made to the file since last commit)
git commit -a -m "Change" ( Skip staging and commit direclty. Add changes from all traced files only. Untraced files are not added)
git reset --soft HEAD^ -  (Undoing commit and reset into staging [^ Move one commit before HEAD] )
git add todo.txt
git commit --amend -m "Some message" ( Add to last commit. Overwrite last commit. Whatever has been staged is added to last commit)
git reset --hard HEAD^ ( Undo last commit and all the changes)
git reset --hard HEAD^^ (Undo last 2 commit and all the changes)

```
### Remotes
```

git remote add origin https://github.com/dibsy/git-cheatsheet.git ( Adding a remote )
git remote -v ( List all available remote repository )
git push -u origin master ( Push to origin our master branch )
git pull ( pull changes from remote )
git remote add <name> <address> ( Add remotes) 
git remote rm <name> ( To remove remotes )
git push -u <remote_name> <branch> ( push to remote any branch. Useful in when there are mutliple remotes)

```
### Cloning
```

git clone https://github.com/dibsy/git-cheatsheet.git ( Clone a remote repository. Add origin remote pointing to clone URL)
git clone https://github.com/dibsy/git-cheatsheet.git my-repo ( Will be stored in my-repo directory )

```
### Branching
```

git branch new_branch ( Create a new branch )
git checkout new_branch ( Switching to the branch_name )
git checkout master ( Move back to master branch )
git merge new_branch ( Merge the contents of new_branch in master )
git branch -d new_branch ( Delete the branch )
git checkout -b admin ( Fast forward technique. Creates and checksout branch)

Scennario  Based - Creating local branch and sending it to remote
git checkout -b mybranch ( Create and checkout local branch)
git push origin mybranch ( Push local branch to remote)
git add cart.rb			 ( Add the new files)
git commit -a -m "Some message" ( Commit )
git push ( pushed to mybranch)  ( Push )

```
### Merging Changes (Push/pull)
```

Incase the remote commit is ahead of local copy but on different files
git push ( Will throw error)
git pull ( Do git pull first)
git push

Incase the remote commit is ahead of local copy but on same files
git pull ( error )
git status 
edit the file
git add file.txt
git commit -a

```
### Diff
```

git diff ( see the changes made in files)
git diff HEAD^ ( diff with the parent of the latest commit)
git diff HEAD^^ ( diff with the grandparent of the latest commit)
git diff master branchname ( diff two branches )

```
### Tagging
```

git tag ( List all the tags )
git checkout v0.1 ( checkout the commit )
git tag -a v0.2.1 -m "New changes in v0.2.1"
git push --tags ( Push the tags to remote )

``` 
### Removing
```

git rm file.txt
git commit -m "Removing file.txt"

```
### Untracking 
```

Untracking File
git rm --cached somefileToUntrack.txt

```
### Aliasing
```

git config alias.myaliasshorcutcommand commit


```
### Blame
```
git blame somefile.txt ( see who made the changes and other details of the changes)

```

