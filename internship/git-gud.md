## git username hiccup lol
So TIL that if you make any commits to any repo , even work repo , your username shown to other people will be the global git username you had given to git when working with your first project , when you pushed to a remote repo ! 
### to see what your current username is 
```sh
git config --list
```
> you can use it to check if it has changed afterwards too 

### to change it use these commands in terminal 
```sh
Set your username: git config --global user.name "FIRST_NAME LAST_NAME"
Set your email address: git config --global user.email "MY_NAME@example.com"
```
[source](https://support.atlassian.com/bitbucket-cloud/docs/configure-your-dvcs-username-for-commits/) 

## git merge conflicts
So TIL that merge conflicts can be seen when 2 people are working on same branch !
like not only when we **MERGE** 2 branches but also while commiting .

### steps
commit your changes ,
pull the other guy's changes using git pull origin branch_name
now you will have merge conflicts in your vscode .
using buttons u can sellect which changes you want to keep .


### I did not commit !
so I did the same thing (clicked pull) using vscode but my vscode rejected for some reason !! ;(
it showed , [this](https://stackoverflow.com/questions/51817479/vscode-please-clean-your-repository-working-tree-before-checkout) error 
with the following git log/output error

```sh
> git pull --tags origin scenario-one
From https://hehe
 * branch            scenario-one -> FETCH_HEAD
   e1919e0..3a106a1  scenario-one -> origin/scenario-one
error: Your local changes to the following files would be overwritten by merge:
	src/modules/landing/pages/landing-page.tsx
	src/modules/sucess-page/styles/success-page.css
Please commit your changes or stash them before you merge.
error: The following untracked working tree files would be overwritten by merge:
	src/modules/common/components/footer.tsx
	src/modules/common/styles/footer.css
Please move or remove them before you merge.
Aborting
```
### so commit / stashing should be done before pulling to see merge conflicts !
- but why? & what if we don't want to commit yet ?
- This is a question for some other time .
