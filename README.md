# Git 
``__#branch develop __``   
git checkout -b develop  
git add .  
git commit -m "docs: added instruction"  
git push origin develop  
``__#branch first feature__``    
git checkout -b first/feature  
git add .  
git commit -m "feat: extended paragraph  
git push origin first/feature  
``#delete the first feature``   
git checkout develop  
git pull origin develop  
git branch -D first feature  
git push origin --delete first/feature  
``__#branch second feature__``    
git checkout -b second/feature  
git add .  
git commit -m "feat! : gitflow extended"  
git push origin second/feature  
``__#delete the second feature__``    
git checkout develop  
git pull origin develop  
git branch -D feat/second  
git push origin --delete ``second/feature`` feat/second  
``__#branch release__``    
git checkout -b release/0.1.0  
git add .  
git commit -m "chore: bump to release"  
--
``__#merge release branch in both develop and master__``        
git checkout develop  
git merge release/0.1.0    
git checkout master  
git merge release/0.1.0  
``__#création tag __``   
git tag -a v1.0 -m "My tag first version"  
git push origin --tags  
git checkout master  
``__#delete the release branch__``    
git branch -D release/0.1.0  
git push origin --delete release/0.1.0  
