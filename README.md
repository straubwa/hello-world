# hello-world
just another playground test repo

## markdown file syntax
* [markdown intro](https://daringfireball.net/projects/markdown/)
* [markdown command cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* to add multi lines to a bullet list, add 2 trailing spaces to the first line

## common git commands
* git log --oneline --graph
* git checkout [branch name] (switches HEAD to the branch name)
* git fetch (update local branch to match latest from server)
* git merge [branch name] (merges changes from branch name to HEAD)
* git branch -a (lists all remote and local branches)
* git branch -d [branch name] (deletes branch name if all changes have been merged, use -D to force delete)
* git push (pushes changes to github for current branch, use --all for multiple branches)
* git push origin :[branch name] (deletes a remote branch that was deleted locally first and tracked)
* git push -u origin [branch name] (pushes local branch to create a new remote branch with same name and makes local trackable)
* git reset  
  git checkout .   
  git clean -fdx (these three commands will remove any uncommited changes in the current branch - basically an undo)
* git mv [current path]/* ./[new path] -k (moves files from current path to new path and stages all changes)
* git add -A (stages all changes - new/changed/deleted)
