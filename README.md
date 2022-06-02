## Deployment
After creating and setting up a repo  
__On develop branch__
```bash
git checkout -b develop
git add .
git commit -m "docs: added instruction"
git push origin develop
```
__Branch feature first__
```bash
git checkout -b feature/first
git add .
git commit -m "feat: extended paragraph"
git push origin feature/first
```
__Delete feature first__
```bash
git checkout develop
git pull origin develop
git branch -D feature/first
git push origin --delete feature/first
```
__Branch feature second__
```bash
git checkout -b feature/second
git add .
git commit -m "feat! : gitflow extended"
git push origin feature/second
```
__Delete feature second__
```bash
git checkout develop
git pull origin develop
git branch -D feature/second
git push origin --delete feature/second
```
__Release branch__
```bash
git checkout -b release/0.1.0
git add .
git commit -m "chore: bump to release"
```
__Merging release branch on develop and master__
```bash
git checkout develop
git merge release/0.1.0
git checkout master
git merge release/0.1.0
```
__Tag creating__
```bash
git tag -a v1.0 -m "My tag first version"
git push origin --tags
git checkout master
```
