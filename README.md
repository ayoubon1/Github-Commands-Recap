# maps
git init
git add .
git commit -m "init the repo"
git remote add origin htttps.....
git push -u origin master
#branch develop
git checkout -b develop
git add .
git commit -m "docs: added instruction"
git push origin develop
#branch first feature
git checkout -b first/feature
git add .
git commit -m "feat: extended paragraph
git push origin first/feature
#delete the first feature 
git checkout develop
git pull origin develop
git branch -D first feature
git push origin --delete first/feature
#branch second feature
git checkout -b second/feature
git add .
git commit -m "feat! : gitflow extended"
git push origin second/feature
#delete the second feature
git checkout develop
git pull origin develop
git branch -D second/feature
git push origin --delete second/feature
#branch release
git checkout -b release/0.1.0
git add .
git commit -m "chore: bump to release"
git push origin release/0.1.0
#merge release branch in both develop and master 
git checkout develop
git merge release/0.1.0
git checkout master
git merge release/0.1.0
#création tag
git tag -a v1.0 -m "My tag first version"
git push origin --tags
git checkout master
#delete the release branch
git branch -D release/0.1.0
git push origin --delete release/0.1.0
