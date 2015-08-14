
# Portfolio
Jason Woods Portfolio

Deployment Plan
====================================

This plan is for deploying to both Stage and Production enviroment.

Stage
-------------------------

1. $git checkout stage
	a. This will checkout to the stage branch from master branch.

2. $git pull origin stage
	a. Pulls the latest from github master branch.
	b. Resolve any conflicts
		1. After resolve need to commit changes.
			a. $git add .
			b. $git commit -am 'Merge message'
			c. $git pull origin master'

3. $git merge master branch
	a. Resolve conflicts (see 2.b.1)

4. Test locally 

5. $git push origin stage

6. Tag Release 
	a. git tag -a v.1.X.RC -m'Feature that is changing'
	b. git push origin --tags

7. Push to stage server
	a. $git push stage stage
	b. Test at http://45.55.1.187/



Master
-------------------------

1. $git checkout master
	a. This will checkout to the stage branch from stage branch.

2. $git pull origin master
	a. Pulls the latest from github master branch.
	b. Resolve any conflicts
		1. After resolve need to commit changes.
			a. $git add .
			b. $git commit -am 'Merge message'
			c. $git pull origin master'

3. $git merge stage branch
	a. Resolve conflicts (see 2.b.1)

4. Test locally 

5. $git push origin master

6. Tag Release 
	a. git tag -a v.1.X.X -m'Feature that is changing'
	b. git push origin --tags

7. Push to Production server
	a. $git push prodServer master
	b. Check at http://192.241.231.237/


Communicate New Deployments
------------------

Before any deployments to staging or production server check with team members to verify that you can push. This will prevent any confilcts and potential failures. 




