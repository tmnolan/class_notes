#Version control systems
		
###why use version control:

* example of why you might want to use - for grant proposal or manuscript to avoid having so many different files representing the versions
	* Gource to visualize the workflow - execute in git repository to show an animation of what was done - **should do this for the final group project**
	* options for versioning projects - Git and SVN - any others.
	
	###what version control let's you do:
	
	* Track changes
	* Revert entire project or single file to prev. version
	* Look at changes over time
	* View who made changes and blame them for bug if needed.
	* have multiple branches to make changes without affecting others work.
	 
	### Using git
	* staging files with git add
	* git commit
	* these happen locally and then can be added into remote host. 
	* with remote
		* pull
		* fetch
		* clone
		* push - send your changes back
	* **web based**: 
		* GitHub - most common free public repositories and paid private. 		Over 1GB discouraged
		* **Bitbucket** - unlimited public and private repos. register 		with .edu email and get unlimited collaborators on private repos
		* Gitlab - also free public and private and up to 10GB repo.
		
		### limitations of git
		* when repos get large git gets slow
		* works best with txt files , but not with binary (e.g. not good 		for MS word)

# Working in Git

### cloning a repo
* **git clone repourl**
* **to update**: git pull origin master. **DONT DO THIS ON BRANCH OTHER THAN MASTER** otherwise your new branch will be replaced with master.
* **git status**: what branch and what changes you've made\
* **git diff** : see what changed
* **git diff filename** : for only one file
* **git checkout filename** : restores that file to the last time updated
* **git checkout newbranchname** : switch to different branch

### Setting up a Repository 

* `git init directory_name`
* `git commit -am "message"`  
	*  -am option combines git add and git commit and lets you write a message. 
* **set up remote**: `git remote add origin git@github.com:username/repo-name.git` 
	* another way is to just make a repo online with README.md and then clone it to your computer
* should always pull before you push
* git push -u origin master 
	* **repo must be already made online**
* **git add** : can add everything in directory and subdirectories using: 
`git add . `
* setting up git ignore:
	use : `.gitignore file`
	
	or set up global ignore: `~/.gitignore_global`
	
* **make git aliases**: Use aliases. You can add specific aliases for Git commands in the .gitconfig file that lives in your home directory.
	* examples I added:
	* git hist : shows nice tree of history
	* last = log -1 HEAD
	* ci = commit
	* st = status

* Git GUIs: SourceTree is recommended. 

### Fixing confilts
* if you are working on things and someone else is then you have confilt
	* git duplicates the lines - **search for HEAD to find them** 
	* then you need to resolve the confilts and remove the lines that git added to show you where they are. Then you can push the repo
	* When working on manuscripts you should seperate lines so that they don't generate merge conflicts. Also communicate with collaborators. 





		

	

