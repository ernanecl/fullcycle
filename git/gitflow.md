### gitflow commands
#### start repository with gitflow
```
git flow init
```
#### create feature branch
```
git flow feature start <branch_name>
```
#### merge with the develop branch
```
git flow feature finish <branch_name>
```
#### create release branch
```
git flow realease start <branch_name>
```
#### merge the release branch with main and develop
```
git flow realease finish <branch_name>
```
#### create hotfix branch
```
git flow hotfix start <branch_name>
```
#### merge the hotfix branch with main and develop
```
git flow hotfix finish <branch_name>
```
