Sandbox
-------

a repo for learning git and trying out various commands

###Changes made in multiple files, some files need to go to a remote branch, others should stay in the working tree and not pushed until work is complete on them

foo.txt - changes in this file should stay in the working tree
bar.txt - changes in this file should go to a remote branch named 'improvements'

```bash
git stash # puts all files into a stash, and undoes changes in the working tree
git checkout stash@{0} -- bar.txt # pulls out just the file that you want to put in the branch
git checkout -b improvements # creates a new branch named 'improvements' and switches to it
git commit -m "made improvements" # commits changes in bar.txt to current branch (improvements)
git push origin improvements # pushes the local improvements branch to the remote named 'origin'
git checkout master # switches back to master
finish work on foo.txt
git commit -am "finally got foo.txt working" # commits foo.txt to local master branch
git push # pushes foo.txt to master branch on origin remote
```
