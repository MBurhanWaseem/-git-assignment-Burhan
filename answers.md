# Git Assignment — Answers


### ANSWER1:terminal: in termibal we write commands and tell the computer what to do.
             while clicking the folder is the long task and it cant do everything for you.

### ANSWER2:(a) list all files including hidden ones:ls -A
##         (b) create a folder called project:mkdir
##        (c) move into that folder:cd


### ANSWER3: What does the cd .. command do? What about cd`: cd.. takes us the one directory back. and the cd~ takes us back to the starting directory.


### Explain what version control is in your own words. Give one real-world analogy (not
Google Docs — pick your own)??
---- version controls is a system that recoreds every change which is done to the files. we can see who changes what, when and why.
### ne real-world analogy::
-it is like the working on the final year thesis.instead of making files for every change we make one file with the  message like fixed reference.

### What is the difference between Git and GitHub? Can you use Git without GitHub?
--- git is the tool that track the changes and github is the platform that creates repositories.yes we can use git without the github.git works fully locally.

### Name three features GitHub provides that Git alone does not?
--- pull thge request
--- project collaborations
--- cloud hosting.

### What is a repository? What is the difference between a local repository and a remote
repository?
--- a repository is a folder that git tracks. it contains all the projects file.
 local repository: the repo on our computer
 remote repository: the copy stored on a server.it is used for backup and sharing.
 
### Explain what HEAD means in Git. What happens to HEAD when you switch branches?
--- head is like a marker. it tells us where we are and which branch on we are,
--example: if head is in the main and we switch to the other feature now head moves to that feature.
### What is a .gitignore file? Write a .gitignore that ignores: all .log files, a folder
called node_modules/ , and any file ending in .env .??
---.gitignore is a filer that tells git which files or folder to not trak. it is used for secrets files that we donot want to share.
.log
 --Ignore any file ending with .env
 *.env
 .env
 **/.env



#### Why did we commit A+B separately from C? When would you
want to split commits this way?::: We commit a and b  and then c sepertely because a and b doing the same work and the c did the different work. we want split commits this way when we want to do different workfrom different files.

#### In answers.md , answer: What would happen if you made a local commit first WITHOUT
pulling? What command helps you check?:::: if we made a local commit first there will b a conflict if someone do a work seperately there will be the conflict.

#####  In answers.md : Did this merge create a merge commit or was it a fast-forward? How
can you tell? :: it was a fast forward. i can tell by see the cmd message.

#### What is the purpose of a pull request? Why not just merge directly?
###     a pull request is a request to merge code after review. it allows teammembers to review code. we dont merge directly to protect main from broken code

### Name two things a reviewer should check in a pull request?
---- correctness and logic
---- code quality and safety


#### What is the difference between a merge commit and a fast-forward merge?
--- fast forward merge happens when main has no commits since the branch was created.
--- merge commit happens when both main and the features branch have diverged.



-----------------------------------------PART 5 SCENARIOS------------------------------------------


### Scenario A. Ahmed creates a branch and changes line 10 of index.html . Sara creates a
different branch and changes line 1 of the same index.html . Both merge into main . Will
there be a conflict? Why or why not?

-- no conflict. because ahmad change the line 10 and the sara change line 1 on different branch.conficts happens when same line are edited differently.




### Scenario B. Ali edits style.css on his branch. Fatima edits app.js on her branch. Both
merge into main . Will there be a conflict? Why or why not?

--No conflict. because they both edited two completely different files. git will take both files and merge automatically.



### Scenario C. DevA changes line 5 of config.py to DEBUG = True . Dev B changes line 5 of
config.py to DEBUG = False . Both merge into main . Will there be a conflict? If yes,
show exactly what the conflict markers would look like in the file.

-- ys here is the conflict.because they both changes the exactly same line.git confused which line is is correct.
<<head
Debug=True
Debiug=False
>>feature branch name
head is the current branch devA change,. below is the incomming branch. we must manually edit and keep one.

### Scenario D. You run git merge feature/new-ui and see this output:
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
Write out the exact steps (commands included) you would take to resolve this conflict
and finish the merge.


---git status
-- open index.html in vs code and find the conflict makers
---git add .
-- git commit -m "ix the resolve"



### Scenario E. Your teammate says: "I always do git pull before I start working every
morning." Is this a good practice? Explain why or why not, and what could go wrong if they
skip it.

yes it is very good practice and is highly recommended-
it is good because it gets the latest change from the main. it avoids the merger conflicts.

--- if we skip it we work all day on the wrong code. if we try to push we get rejection.it has the higher chance of getting the large merger


--best flow: get checkout main, get pull origin main,git checkout
