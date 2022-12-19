# Git-GitHub-Crash-Course-2023

https://www.youtube.com/watch?v=ulQA5tjJark

https://github.com/academind/github-actions-course-resources.git

What is Git ?
Version Control System 
Manage Source Control Changes 

Commits - Save code snapshots 
Branches - Work with alternative code versions
Checkouts - Move between branches and commits 

With Git, you can easily roll back to older code snapshots or developer new features without breaking production code 

What is GitHub 
Cloud git repository 
Code management and collaborative development 
“Issues”
“Projects”
“Pull requests” 

Automation and CI/CD - Github Actions, Apps and more


Git Repositories 
Git features can be used in projects with Git repositories 

A repository is a folder used by Git to track all changes of a given project 
Git commands require a repository in a project 

Create Git Repositories via git init 
Only required once per folder / project 

Some projects initialize Git for you 
e.g. React projects 

Terminal 
git add Index.html 
clear

git init 
Initialized empty Git repository in C:/Users/Matheus/Desktop/Rodrigo/Visual Studio Code/Academind/Git & GitHub Crash Course 2023/.git/

Working with commits ( Code Snapshots ) 

Create Commits 
git add <files(s)>
Stage changes for next commit 
git commit 
Create a commit that includes all staged changes 

Terminal 
git add index.html
git status 
git commit 

git commit -m “initial commit ”
git log 

Move between Commits
git checkout < id >
Temporarily move to another commit 
clear

git add index.html 
git status 
git commit -m “added link link to Git docs.”
clear 
git log 
git checkout 6223f…
git log
git checkout main 
clear
git log 

Undo commits 
git revert < id > 
Revert changes of commit by creating a new commit

clear
git revert 15ad1…

Reverting:add link 

git log 

git reset - - hard < id >
undo changes by deleting all commits since < id > 


clear 
git reset - - hard 6223f…
git log

git init - Initialize a Git repository ( only required once per project )
git add < files ( s) > - Stage code changes ( for the next commit )
git commit -m “...” - Create a commit for the staged changes ( with a message ) 
git status - Get the current repository status ( e.g. which changes are staged ) 
git log - Output a chronologically ordered list of commits
git checkout < id > - Temporarily move back to commit < id >
git revert < id > - Revert the changes of commit < id > ( by creating a new commit )
git reset < id > - Undo commit(s) up to commit < id > - by deleting commits 

git add index.html styles.css logo.png 
git add . 
git status
On Brach main 
Changes to be committed: 
( use “git restore - - staged <file>...” to unstaged  ) 
new file: .gitignore 
new file: index.html 
new file: logo.png 
new file: styles.css

clear 

git commit -m “add logo and styling”  

Understanding Git Branches 
git log 
main ( more than one branch ) c1 / c2 
create new branch - git branch < name > feature-1 / c2 
c3 / c2 - c4 - c4 ( merge branches ) git merge < name > 

Terminal 
git branch feature-restructure 

git branch 
feature-restructure
*main 

git checkout feature-restructure 
Switched to branch ‘feature-restructure 
clear 
git log

git checkout main 
Switched to branch ‘main’ 
git branch 
feature-restructure 
main 
git branch -D feature-restructure 
Deleted branch feature-restructure  ( was 176be24 )
git branch 
main 
clear 

git checkout -b feature- restructure 
Switched to a new branch ‘feature-restructure 
git branch 
*feature-restructure 
main 
git log
clear
’
git branch 
* feature-restructure 
main 

git add . 
git commit -m “added links and restructure page”
[feature-restructure 8789eb0] added links and restructure page
git log 
clear 

git checkout main 
Switched to branch ‘main’
git log
clear 

git add . 
git commit -m “changed title
git log
git branch
feature-restructure
*main 
git checkout feature-restructure 
Switched to branch ‘feature-restructure 
clear
git checkout main 
Switched to branch ‘main’
git merge feature-restructure

git checkout main
Switched to branch ‘main’
git merge feature-restructure 
Auto-merging index.html 
Merge made by the ‘ort’ strategy. 
index.html - 15 +++++++++–
styles.css - 4++++
2 files changed, 16 insertions(+), 3 delections(-) 

git log 
clear

git branch 
feature-restructure
*main 
git checkout feature-restructure 
Switched to branch ‘feature-restructure 
clear 

git checkout main 
Switched to branch ‘main’
git branch 
feature-restructure
*main 
git branch -D feature-restructure 
Deleted branch feature-restructure ( was 8789eb0 ) 

Github Repositories 
Cloud storage for your Git repositories - Backup, cross device usage, collaboration 
Public
Private 
“Connect” to local Git repositories via - git remote add
Local commits are uploaded via - git push 
Remote commits are downloaded via - git pull 

Terminal 
clear 
git remote add origin

git push 
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use 
git push - - set upstream origin main 

git branch 
*main 

git push origin main 
fatal: unable to access 
clear

git remote set-url origin maxacademind1@github.com/maxacademind1/github-crash-course.git 
clear
git push origin main 
password 

https://git-scm.com/docs

git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use 

git push - - set upstream origin main 
git push - - set upstream origin main 
clear 

git push
Everything up-to-date 

git add index.html
git commit -m “added section”

git push origin feat-section
clear

git checkout main 
git merge feat-section 
git push 
clear

git branch
feat-section
*main
git branch -D feat-section 
Deleted branch feat-section ( was 00d184e )
clear

git pull 
 
Github 
git config - - global user.name “maxacademind”
git config - - global user.email “dummy-user2@academind.com”


git clone https://github.com/maxacademind1/github-crash-course.git git demo
git remote 
origin 
git remote get-url origin 
https://github.com/maxacademind1/github-crash-course.git
clear 
git checkout -b feat-color
Switched to a new branch ‘feat-color’
git add . 
git commit -m “changed title color” 
[feat-color 8d988e0] change title color 
1 file changed, 1 insertion(+), 1 deletion(-) 
clear 
git push origin feat-color 
remote: Permission to maxacademind1/github-crash-course.git to maxchwarzmuller. 
fatal: unable to access ‘https://github.com/maxacademind1/github-crash-course.git/’: The request url returned error: 403

issue 
Suggestion: Change title color 
Write 
I think it looks better if the main title is a bit more orange.
The style rule could be change like this:
‘’’css
h1{
   color: #efa82e;
}
‘’’ 
Preview:
I think it looks better if the main title is a bit more orange.
The style rule could be change like this:

h1{
   color: #efa82e;
}

Settings 
Collaborators 
Add people 
Add a collaborator to github-crash-course 
maxacademind2 
Add maxacademind2 to this repository 
Accept invitation 
Branches 
Branch protection rules
Add branch protection rule
Branch name pattern
Main 
Protect matching branches 
Require a a pull request before merging 
Creat

git remote set-url origin 
 ‘https://maxacademind2@github.com/maxacademind1/github-crash-course.git
git push origin feat-color

Settings 
Developer settings 
Personal access tokens 
Create a new token
New personal access token 
Note / Demo 1 
Repo permissions 
Generate Token 
Copy token 
ghp_623… Ctrl p 
clear

git checkout main 
Switched to branch ‘main’ 
Your branch is up to date with ‘origin/main’ 
git merge feat-color 
clear 
git push origin main 

remote:error… 

new pull request 
base: main 
compare: feat-color 

Write 
I change the title color as suggested in #1
Preview 
I change the title color as suggested in #1
Create pull request 
Add your review 
Review changes
Submit review 

Closes #1
Comment 
Merge pull request 
Confirm merge 

issue 
Suggestion: Change title color 
mark as 
Close 

git pull
git pull
git checkout fear-color 
m styles.css
Switched to branch ‘feat-color ’
clear

git add styles.css
git commit -m “broke code”
[feat-color d2e1d54] broke code
git push origin feat-color 
remote: Permission to maxacademind1/github-crash-course.git to maxchwarzmuller. 
fatal: unable to access ‘https://github.com/maxacademind1/github-crash-course.git/’: The request url returned error: 403

fork 
Create a new fork
Owner
Create fork 
git clone https://github.com/maxacademind1/github-crash-course.git git-demo2

git remote set-url origin  https://maxacademeind2@github.com/maxacademind1/github-crash-course.git

git checkout -b ‘feat-link-color’ 
clear 
git add styles.css
git commit -m “ change link color ”
[feat-link-color b37699c] change link color 
git branch
* feat-link-color 
git push origin feat-link-color 

maxacademind1/github-crash-course 
pull requests 
new pull request 
Compare across forks

create 
Changed link color since it looks nicer. 
create pull request 

reviewer 
Add your review 
Review changes 
Approve 
Submit review 
Merge pull request 
Confirm merge


 






