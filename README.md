# method to change root
This worked for me, and kept all my history intact. From the incorrect root folder (from https://stackoverflow.com/questions/1918111/my-git-repository-is-in-the-wrong-root-directory-can-i-move-it-instead-of):

- Move the folder:

`mv .git thecorrectfolder/`

- Re-initialize the git repo:

`cd thecorrectfolder/`

`git init`

- Re-add all the files, commit, and push:

`git add .`

`git commit -am 'fixing things'`

`git push origin master`

- Done! Get yourself a beer.

When you commit the git repo after re-initializing, you'll get a bunch of output that looks like this:

rename {ethanode/coffee => coffee}/app.coffee (100%)
In other words, all of your references from the parent folder and being renamed to use the correct folder.

