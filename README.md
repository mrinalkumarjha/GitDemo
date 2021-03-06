# To install Git test content from master
	go to git-scm.com > download  git and install it
	
# Git configuration globally 
	git config --global user.name "your name"
	git config --global user.email "youremail@domain.com" 
# Git initialization
	git init demo  : to initialize empty git repo locally inside demo folder
	ls -al to list all file and folder inside repo

# Git Local state
	Three local state of git in local
	1: Working Directory : it contains all files and folder of application
	2: Staging Area : this is state where files are moved from working directory
	3: Repository(.git folder) : It holds all commited data
	4: Remote : This remote state itself contain above three state
	
# To Push code from working dir to staging area
	git add test.txt : this will push test.txt to staging state
	
# To Add file to Repository state from staging
	 git commit -m 'adding new test1.txt'   : this will push file from staging to repository state

# Repository And  Git folder
	The actual git repo exists inside .git directory
	 cd .git/  : To change directory to .git. this is special directory maintained by git internally.
	 ls -al  : to display all list inside .git folder
	 rm -rf .git : To remove git directory. after this .git will be removed
	 git init . : To add .git folder again to maintain versioning. this will complete new.
	 git add . : to add all file to git working area 

# To check log like how much commit we have added
	git log : it will list all commit that is part of this repository
	git show (commit id)39da54c0029b4a8f98686e2c33326cc89e33d39a   : to show all details of commit

# Now to commit modified file in single command without adding we use -am (add message) 
	git commit -am "added some new command" : this will add and commit also
	
# To back out changes (the changes need to be removed after adding to stage)
	git reset HEAD README.md   : This will remove file from stage area to working
	git checkout -- README.md   : thihs will remove all changes and put file in last working state
# To check config detail
	git config --global --list   : it will show user details
	
# To Add Rename or DELETE file after commiting locally
	git mv example.txt demo.txt  : it will rename example.txt to  demo.txt in repository locally. this is staged changes
	to commit it agin we use commit a=commang git commit -m 'renaming file'
	
	git rm demo.txt  : to delete file , this will stage change. to complete change we need to commit
	git commit -m 'deleting file'
	
	touch newfile.txt : add new file

# Excluding unwanted files and folder from git repo
	1: create .gitignore file  : touch .gitignore
	2: write command per line to exclude
	ex : *.log to exclude all file with log

# Types of Merge
	Fast-Forward : this is simple merging when there is no changes detected in master branch. It will simply apply all 
	commit to master branch. we can disable this option if undesirble result expected.
	
	Automatic Merge: 
	
	Manual merge : This has to be done when git unable to do automatic merge. All conflict must be resolved 
	before merging.
# Markers (Pointer) : 
	HEAD is most used pointer which point to last commit of current branch.
	
# Branching 
	
	Branches allow us to work on different version of same files in parellel. one branch can be independent from
	other branches. we can later decide to merge changes to two branches. branches resolves seperation of version of 
	same files. Head is pointer which point to branch latest branch.
	ex we can have production branch, development branch, a branch to work on bug fixes.


	git checkout -b updates  : It will create new branch and switch to updates branch.
	
	To merge update branch to master first we need to switch to master branch then use command from master branch
	
	git merge updates  : to merge updates branch changes to master
	
	git branch -d updates  : to delete updates branch.
	
	// delete branch locally
	git branch -d localBranchName

	// delete branch remotely // master changes
	git push origin --delete remoteBranchName

# Conflict resolution
	it happens when many people work on same file and change on same line. 

# To list all branch
	git branch

# To Create branch 
	git branch develop
	
	or to create feature branch : it will take ref of develop branch and create feature branch
	git checkout -b feature/new-feature-branch

# To checkout develop branch : now master will be Switched to branch 'develop'
	git checkout develop

	
# To switch branch
	git checkout master : to get into master
	git checkout develop : to get into develop

# To mearge feature branch to develop
	git merge feature/new-feature-branch


# To populate commit detail
	git show bb35602a5f12da7027d55bd1a1e1859de79b97f6

# To push develop branch to server
	git push --set-upstream origin develop

# delete branch locally
	git branch -d localBranchName

# delete branch remotely
	git push origin --delete remoteBranchName

# To clone remote git repository to local
	git clone https://github.com/mrinalkumarjha/GitDemo.git FolderNameToClone
# To check repository of git
	git remote -v
# To Push changes to github
	git push origin master

# Difference between FETCH AND PULL
	Doing fetch and pull before any push is good practice. 
	git pull does a git fetch followed by a git merge. A git pull is what you would do to bring a local branch up-to-date with its 		remote version, while also updating your other remote-tracking branches.
	
	When you use pull, Git tries to automatically do your work for you. It is context sensitive, so Git will merge any pulled 		commits into the branch you are currently working in. pull automatically merges the commits without letting you review them 		first. If you don’t closely manage your branches, you may run into frequent conflicts.

	When you fetch, Git gathers any commits from the target branch that do not exist in your current branch and stores them in your 	local repository. However, it does not merge them with your current branch. This is particularly useful if you need to keep your 	repository up to date, but are working on something that might break if you update your files. To integrate the commits into your 	 master branch, you use merge.
	
# To show remote detail
	git remote show origin

