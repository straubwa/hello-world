## markdown files
* [markdown intro](https://daringfireball.net/projects/markdown/)
* [markdown command cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* to add multi lines to a bullet list, add 2 trailing spaces to the first line

## git 
### commands
* git log --oneline --graph
* git log --oneline --graph origin/[branch name] (run this after a fetch to see list of changes to merge)
* git clone [url] [folder name] (creates local copy of existing repo at url in a subfolder of the current path, folder name is optional - if not used, will take the name of the repo as the folder name)
* git remote add origin [url]  
* git checkout [branch name] (switches HEAD to the branch name.  this is the way to switch between existing branches)
* git checkout -b [branch name] (creates a new branch and switches HEAD to the branch name)
* git fetch (update local branch to match latest from server, but does not move local branches)
* git fetch -p (removes remote branches that no longer exist on remote)
* git pull (does a fetch plus merge)
* git merge [branch name] (merges changes from branch name to HEAD)
* git branch -a (lists all remote and local branches)
* git branch -d [branch name] (deletes branch name if all changes have been merged, use -D to force delete)
* git push (pushes changes to github for current branch, use --all for multiple branches)
* git push origin :[branch name] (deletes a remote branch that was deleted locally first and tracked)
* git push -u origin [branch name] (pushes local branch to create a new remote branch with same name and makes local trackable)
* git push --set-upstream origin master (associate a local repo with blank repo at the url, ex. github, and push commits to the url)
* git reset  
  git checkout .   
  git clean -fdx (these three commands will remove any uncommited changes in the current branch - basically an undo)
* git mv [current path]/* ./[new path] -k (moves files from current path to new path and stages all changes)
* git add -A (stages all changes - new/changed/deleted)
* git config -l (lists all config key value pairs)
* git config --global [key.name] [value] (create/edits key value pair, key tends to have a ".", ex. user.name, global is scoped to user on this machine)
* git status (lists what has been staged, changed, new/delete)
* git add -A (moves all changed files to staged)
* git reset (moves all staged files to changed)
* git commit -m "[commit message]" (commits staged changes locally with the commit message)
* git commit -am "[commit message]" (adds changed to stage and commits locally)
* git add -u (stages all updated changes)
* git config --global alias.[alias name] "[command to alias] (create an alias for commonly used commands, such as "log --oneline --graph")

### git aliases
* lga = "log --oneline --graph"
* you can append info after an alias, ex. "git lga origin/[branch name]" will run "git log --oneline --graph origin/[branch name]"

### setup / config
* need to setup user.name and user.email on machine in order to do a commit
* verified commits on gitgub
  * to have commits show up on github as "verified" need to sign commits with GPG
    * otherwise you can have commits from what looks like anybody you like just by setting user.name and user.email
  * [github howto setup signing commits](https://help.github.com/articles/signing-commits-with-gpg/)
  * [step by step setup](https://jamesmckay.net/2016/02/signing-git-commits-with-gpg-on-windows/)
    * install [gpg4win](https://www.gpg4win.org)
    * create key in Kleopatra
    * run git commands  
      git config --global user.signingkey [Key-ID]  
      git config --global commit.gpgsign true  
      git config --global gpg.program "C:\Program Files (x86)\GnuPG\bin\gpg.exe"
    * follow steps on [adding new GPG key to Github](https://help.github.com/articles/adding-a-new-gpg-key-to-your-github-account/)
* initial push of a repo to new github repo
  * create github repo
  * git remote add origin [github repo url]
  * git remote -v (verifies url)
  * git push origin master
* [github add license file](https://help.github.com/articles/adding-a-license-to-a-repository/)

## node.js / npm
* [node](https://nodejs.org/en/)
* [npm](https://www.npmjs.com/)
* [simple getting started with npm](http://nodesource.com/blog/an-absolute-beginners-guide-to-using-npm/)
* npm list -g --depth=0 (lists globally installed NPM packages and version)
* npm install npm@latest -g (to globally update of the version of npm on your machine, instead of "npm i npm" which installs the latest version within the directory that it is run from)
* npm ls (lists all packages in a tree view)
* npm i (downloads all modules listed in project.json file to node_modules folder)
* npm outdated (lists all modules that have a newer version than what referenced in packages.json file)
* npm update (updates all modules to the "Wanted" version as shown in outdated - not necessarily the latest)
* npm prune (finds all modules in node_modules that are not listed in packages.json file)
* npm audit (reviews all packages for known security vulnerabilities)

## angular cli
* ng new [app name] (creates a new angular web app)
* ng serve (starts up the web app to run on localhost:4200)
* ng g component [path]/[component name] --flat=true (creates component files in the folder path stated - format [component name].component.html/spec.ts/ts/css)

## vscode
* [end] (brings out outside of brackets you are in)
* [ctrl]+[c] (ends an "ng serve" session and returns a prompt in the terminal window)

## docker
* docker-machine ip (shows ip of vm that docker resides in)
* docker-machine env (display docker client setup commands)
* docker version (displays info about the version and OS)
* docker info (see what is happening on a docker machine)
* docker pull [image name] (downloads docker image from dockerhub)
* docker images (lists all images downloaded to machine)
* docker ps -a (lists all containers and state on a machine)
* docker run -d -p [external ip]:[ip in container] [image name] (starts up a container for the passed image, if a sha256 is not returned, something is not right)
* docker stop [container id | name] (stops a container from running)
* docker rmi [image name]:[version] (remove a docker image from the local store)

* more info can be found at [Dan Wahlin's useful commands](https://github.com/DanWahlin/Angular-RESTfulService/blob/master/.docker/useful-commands.md)

## other
* [quicktype - generate code from JSON](https://app.quicktype.io/#l=cs&r=json2csharp) online tool to convert json to classes in c#, javascript, typescript, etc...
