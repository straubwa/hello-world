# hello-world
Using this to keep track of common development commands / quickstarts / etc...

## markdown files
* [markdown intro](https://daringfireball.net/projects/markdown/)
* [markdown command cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* to add multi lines to a bullet list, add 2 trailing spaces to the first line

## git commands
* git log --oneline --graph
* git checkout [branch name] (switches HEAD to the branch name)
* git fetch (update local branch to match latest from server, but does not move local branches)
* git pull (does a fetch plus merge)
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
* git config -l (lists all config key value pairs)
* git config --global [key.name] [value] (create/edits key value pair, key tends to have a ".", ex. user.name, global is scoped to user on this machine)


## node.js / npm
* [node](https://nodejs.org/en/)
* [npm](https://www.npmjs.com/)
* npm list -g --depth=0 (lists globally installed NPM packages and version)

## angular cli
* ng new [app name] (creates a new angular web app)
* ng serve (starts up the web app to run on localhost:4200)

## vscode
* [end] (brings out outside of brackets you are in)
* [ctrl]+[c] (ends an "ng serve" session and returns a prompt in the terminal window)