# git setup

## Add remote
`git remote add lab1 git@github.com:HALtheWise/POE-lab1.git`

## Initially merge in history
`git merge -s ours --no-commit lab1/master`
`git read-tree --prefix=lab1/ -u lab1/master`
`git commit -m "Read lab1/master into origin/master subdir"`

## Pull changes from subproject to main project
`git checkout master`
`git fetch lab1`
`git pull -s subtree lab1/master`

## Pull changes from main project to subproject
`git checkout lab1`
`git pull lab1 master:lab1`
`git merge -s subtree master`
`git push`