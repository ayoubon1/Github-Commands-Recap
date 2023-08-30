### Made By Ayoub Khouadri
## Versionning the right way
After creating and setting up a repo 
```
git init 
git commit --allow-empty -m "🎉 init master branch"
git remote add origin <link to gihtub new repo>
git push -u origin master
```
> till this stage the master branch is set up and ready with an empty commit

__Create & init a develop branch__
```bash
git checkout -b develop   # create a new branch called develop = création d'une branche intitulé develop
git commit --allow-empty -m "🎉 init develop branch"
git push origin develop
```
__Branch feature first__
```bash
git checkout -b feature/first
# the branch introducing the first feature is created .
# make the necessary modifications on your project
git add .   # we add all the modification , we must verify in the case of a project the .gitignore file is created .
git commit -m "feat: 🚧 add the project boilerplate" 
git push origin feature/first
```
> After this push we create a pull request & compare it to develop branch

__Delete feature first__
```bash
git checkout develop  # transfer you repo to develop branch
git pull origin develop  # pull modification between distant & local branch
git branch -D feature/first  # this command inorder to erase the branch feature/first locally.
git push origin --delete feature/first # this command inorder to erase the branch feature/first on gihtub distant repo.
```
__Branch feature second__
```bash
git checkout -b feature/second
git add .
git commit -m "feat!: gitflow extended"
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
