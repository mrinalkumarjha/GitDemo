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
	
# to chenge back to master
	git checkout master