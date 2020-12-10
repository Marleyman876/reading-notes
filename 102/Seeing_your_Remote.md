# Seeing your Remote 

Colloboration is a big part of being a succesful coder. Git allows multiple developers to work on the same code.
Git commits changes to the repository in real time by taking snapshots in real time, its like having a Save as for code. Git hold on to. 
Each commit or snapshoot has a label that point to it. 
It is highly recommend that you leave messages on snapshots as a way to point to exactly what was done. 

A remote repository is one that can be accessed from anywhere. There are different ways to see your remote, using specific commands. 

+ `git remote -v` allows you to view all remote repository that your local machine is connected to. 
+ `git fetch [remote-name]` allows you to pull data from a remote project. 
+ `git push [remote-name][branch name]` this command changes data in the name of the selected repository and all the way to the local "master branch."

## GitFlow ACP 

+ `git status` tell you the status of you local repository on your machine. 
+ `git add [file name]` is what we use to add unstaged changes to the staging area before commiting them to the repository. 
+ `git commit -m "insert message"` is what we use to make commits to the repository. 

# Using Git in the terminal

create repository using `git clone` form Https clone tab in github.
go to termninal use git clone then url to clone repository
(main)$ on your terminal shows that the terminl is now connected to the repository 
 (main) $ls lists everything in the repository in your machnie 
 
if you run a git status and the file comes back red then the co9mmint has not been made; use `git add filename` to add the document that you have changed. 