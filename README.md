# To install Git 
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
	 

# To list all branch
	git branch

# To Create branch 
	git branch develop
	
	or to create feature branch : it will take ref of develop branch and create feature branch
	git checkout -b feature/new-feature-branch

# To checkout develop branch : now master will be Switched to branch 'develop'
	git checkout develop

# Now to commit new data in single command without adding we use -am (add message)
	git commit -am "added some new command"
	
# To check log like how much commit we have added
	git log
	
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