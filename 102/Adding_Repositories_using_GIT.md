# Adding your Remote Reposotiory Connections Using Git cmds.

Colloboration is a big part of being a succesful coder. Git allows multiple developers to work on the same code.
Git commits changes to the repository in real time by taking snapshots in real time, its like having a Save as for code. Git hold on to. 
Each commit or snapshoot has a label that point to it. 
It is highly recommend that you leave messages on snapshots as a way to point to exactly what was done. 

A remote repository is one that can be accessed from anywhere. There are different ways to see your remote, using specific commands. a few of these commands are:

+ `git remote -v` allows you to view all remote repository that your local machine is connected to. 
+ `git fetch [remote-name]` allows you to pull data from a remote project. 
+ `git push [remote-name][branch name]` this command changes data in the name of the selected repository and all the way to the local "master branch."
+ `git status` tells you the status of you local repository on your machine. 
+ `git add [file name]` is what we use to add unstaged changes to the staging area before commiting them to the repository. 
+ `git commit -m "insert message"` is what we use to make messages based on the changes you've made within the repository. 

You can clone a repository using `git clone + HTTPS` of the repository in the cmd line.
