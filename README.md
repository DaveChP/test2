 I entered a new empty directory and ran:

git clone git@github.com/DaveChP/test2.git

I entered the newly created directory (a clone of the remote repo) and created this file. I will now add and commit this file to local, branch -M to main and push using these:

git branch -M main
git push -u origin main

# this edit made on remote editor

OK, the push worked fine.

While on remote, the file was edited to insert the heading above. It was committed on remote. Back on local I did:

git pull origin main

to bring this file back to local and update. Everything was automatic, no add, commit or merge was needed. When I opened this file locally, the remote heading was there. I then added this text that follows the last heading and will now add, commit and push it.

## another remote edit (just this line)

All good, making a local edit

New clone on remote, created in new directory named as second argument to git clone:

```
git clone git@github.com:DaveChP/test2.git newDirectory
```

## Local Pull, Modify, Push without Merge
This file is in a directory called 'new', which is a local repository cloned from the remote yesterday. I have just pulled the origin using:

```
git pull remote main
```
and was told I'm up to date. Before modifying this file, I made a new branch to work on:

```
git checkout -b newBranch
```

After this edit, I will add and commit these changes but not merge the branch. Instead I will push the branch for review on remote using:

```
git push origin newBranch
```



