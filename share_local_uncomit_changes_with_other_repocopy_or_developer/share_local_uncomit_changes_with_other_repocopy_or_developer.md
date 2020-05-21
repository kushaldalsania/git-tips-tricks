# Sharing local changes (tracked, untracked)
Sometimes it becomes necessary to share our local change set (tracked/untraced file) with another repo copy on same machine or repo on another machine or another developer.
To do this we create a patch file out of local change sets using `git diff`.

`git diff` only includes staged tracked files. Hence we need to stage all files for commit (but do not commit it). Use `git add .` to stage.

## Create a patch file.
`git diff -p --staged --binary > sample.patch`

## Move patch file to repo where changes needs to be applied.  And then apply patch.
`git apply sample.patch`