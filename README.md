# git-practice
Created to practice and explore Git commands and concepts
# git intro
git is a version control system that tracks changes in code over time. It helps developers save versions, collaborate and undo mistakes easily.The below are main purposes of git or version control system
1. Keep history of code changes
2. Work in teams without overwriting each other's work
3. sync code between local and remote
# git termininology/stages
1. Working directory - where you edit files
2. Staging area (Index) - Where you pepare files for commit (git add file_name (single or targeted files)/.(add all files in working direcory))
3. Local repository - Where commits are stored (git commit -m "short description of change")
4. Remote repository - Hosted online (e.g GitHub), synced with git push/pull origin main/master
# git installation
1. Download git in https://git-scm.com/install/ based on your OS and bit
2. run the downloaded file and setup it
# git registration/sign-in
1. Create account in Github if you not have Github account
2. Sign-in to your github if you have Github account
# Configure git username and email
1. Open terminal
2. command git config --global user.name "Your username same as remote"
3. command git config --global user.email "Your email same as remote"
4. command git config --global --list ( For checking the datas)
# Create directory in local
1. open terminal or git bash
2. Place the directory as per your need e.g /c/Users/username/ GitPractice  
3. command mkdir dir_name e.g mkdir practice 
4. command cd dir_name e.g cd practice 
# Repository creation
1. Create repository in remote e.g git-practice
2. Copy the repo link
# Clone the remote repository
// clone creates a full local copy of a remote repository, including all files, branches and history
1. command git clone Repo link
2. command ls - to check the list of files in pwd and whethere it's correctly created or not
3. command echo " To check stages of git, pull and push between local and remote" >> demo.txt - create sample text file
4. command git status - to check stage of file 
5. command git add demo.txt - to list the file in staging/ index to be commited
6. command git commit -m "short message desc" - the list files in staging area will be commited and stored in local git repo
7. command push origin main/master - to push the changes to remote *** First time it will ask authentication
8. go to remote page and refresh the page, then it will be updated
# Basic git commands
1. git init fresh-project // to create and init new git folder
2. nano example.txt // to create example text file, It will be available in local working directory only
3. git status // to know about the status of git repository and files whether in working directory/staging area/local repository
4. git add example.txt // to add example text file to staging area
5. git commit -m "put your commit message" // to add all the staging area files to local repository 
6. git pull origin main // to get latest source from the remote repository
7. git push origin main // to push the updated source from local repository to remote repository
8. git add -am "put commit message" // to do add and commit in one line
9. git add . // to add all the sources in working directory
10. git add -u // to update tracked file only
11. git config --global --list // to list out the git configuration file
12. git config global -e // to open configure file
#Joining an existing project
// fork is a personal copy of someone else's repository,letting you freely experiment and contribute changes back through pull requests
1. fork the project in git remote
2. copy your forked project url
3. clone <url>
# Tracking files
1. git ls // to track listed 
2. git ls-files // to track listed
# History 
1. git help log // to learn all the git history commands
2. git log // to see all the commit history
3. git log --abbrev-commit // same as (2) but which give short id
4. git log --oneline --graph --decorate // which give short and sweet command
5. git log start_id to end _id // to see the commit history in between
6. git log --since="3 days ago" // to get last 3 days commit history only
7. git log --file_name // to know about particular source commit history
# Alias
// It is a custome shortcut for long or frequently used git commands to save time and typing
1. git config --global alias.alias_name "log --oneline --graph --decorate"
2. git alias_name // call long command with short word
# Igonore unwanted files
1. nano .gitignore 
2. put *.log/*.txt/*.html and etc // which will not track the particular extension files
3. put folder_name // Which will skip the mentioned folder name
# Backing out changes
1. nano eg.txt
2. git add eg.txt
3. git reset HEAD eg.txt // to unlist the area
4. git restore eg.txt // same as (3)
5. git checkout --eg.txt
# Renaming and moving files
1. git mv old_file_name new_file_name // to change the file name ***commit is necessary
2. mv old_file_name new_file_name // to change the file name in outside git e.g file manager add&commit required
3. git mv old_file_name new_file_name & git mv new_file_name old_file_name // No add & commit required
4. git mv file_name directory_name // to move one file to another directory
5. git mv file_name .. // to move the file to previous directory // git add & commit necessary
6. change name in outside git e.g file manager you should add and commit
# Deleting files
1. nano eg.txt // create and add
2. git rm eg.txt // to delete file, after commit must
# Visual merge/dif tool
// It helps compare and solve code differences side by side using a graphical interface for easier conflict resolution e.g p4merge
##Download p4 merge
1. Download and run p4 visual merge tool
2. Set the p4 merge address in system variables
3. p4merge // to check in terminal or any
## P4 merge git configuration
1. git config --global merge.tool p4merge
2. git config --global mergetool.p4merge.path "Address of p4merge with p4merge.exe"
3. git config --global mergetool.prompt false
4. git config --global diff.tool p4merge
5. git config --global difftool.p4merge.path "Address of p4merge with p4merge.exe"
6. git config --global difftool.prompt false
## Comparisions

### Prepare example to practice diff
1. nano example.txt
2. Add some contents then add, commit and push It
3. nano example.txt again
4. add some new contents then add and commit only
5. nano example.txt again
6. add some new content then add only
7. nano example.txt again
8. Add some new content only don't add, commit and push
### Comparing working directory and staging area
1. git diff // normal terminal diff
2. git difftool // open visual diff p4merge
### Comparing working directory and git repo
1. git diff HEAD
2. git difftool
### Comparing Staging area and git repo
1. git diff --staged HEAD
2. git difftool --staged HEAD
### Limiting comparisions to one one file or path
1. git diff --README.md
2. git diff --README.md
### Comparing between commits
1. git diff start_id HEAD end_id
2. git diff HEAD HEAD^
3. git difftool HEAD HEAD^
4. git diff id id 
### Comparing between local and remote master branches
1. git diff master origin/master
# Branching and merging
// branching create separate workspace for new work without affecting main; merge combines changes from one branch into another
1. git branch // list only local branches
2. git branch -a // list local and remote branches
3. git branch branch_name // to create new branch
4. git checkout branch_name // to change(switch) the branch
5. git branch -m old_branch_name new_branch_name // to change branch name
6. git branch -d branch_name // to delete branch
7. git checkout -b branch_name // to create new branch and switch to it
## Fast forward merges
// Simply moves the branch pointer ahead because no new commits exist on the target branch
1. git checkout -b example
2. nano index.html // add and commit must
3. git checkout main/master
4. git merge example
## Disable fast forward merges
// forcing git to create a merge commit even if a fast-forward is possible - preserving the branch history
1. git checkout -b example
2. nano index.html // add and commit must
3. git checkout main/master
4. git merge example --no-ff
## Automatic merges
// It happen when branches have no conflicts and git merges them directly and records it with the given commit message
1. git checkout -b example
2. nano index.html // add and commit must
3. git checkout main/master
4. git merge example -m "put commit message here"
## Conflicting merges and resolution
// conflicting merge occurs when two branches change the same part of file
1. git checkout -b example
2. nano sample.txt // add some contents
3. git commit -am "put commit message here"
4. git checkout master/main
5. nano sample.txt // edit different from example branch
6. git add sample.txt
7. git commit -m "put commit message here"
8. git merge example // *** show error automatic merge failed
9. git mergetool // solve the conflicts in UI
10. git commit -m "put commit message here"
11. ls // you can see sample.txt.origin
12. mate .gitignore
13. *.orig // to skip these extension files
14. git add and commit .gitignore
# Cherrypick
// copy specific commit fromone branch and apply it to another branch
1. git checkout -b developers
2. echo "temporary debug: test line" >> demo.txt
3. git add demo.txt
4. git commit -m "fix: add debug line for login issue"
5. git log --oneline // copy last commit id
6. git checkout main
7. git checkout -b bugfix/login-fix
8. git cherrypick -x commit_id // It do not copy entire code to another file need to fix. It just edit the conflict code
# Revert a commit
// createa new commit that undoes the changes from previous(wrong) commit - safe way to undo
1. git checkout revert-bad-change
2. nano demo.txt // add some content
3. git add demo.txt
4. git commit -m "put commit messae here"
5. git checkout main
6. git merge revert-bad-change
7. git log --oneline // note/copy commit id
8. git revert -m 1 id // this for revert from different branch
9. if you do (2,3,4) in the main/master branch and want to revert commit change do (10)
10. git revert commit_id
# Rebase and squash
// rebase moves your commits to start from latest base; squash combines multiple small commits into one clean commit
1. git checkout -b feature/clean-update
2. echo "line A" >> demo.txt
3. git add demo.txt
4. git commit-m "feat: add line A"
5. echo "line B" >> demo.txt
6. git add demo.txt
7. git commit-m "fix: add line B"
8. echo "line C" >> demo.txt
9. git add demo.txt
10. git commit-m "chore: add line C"
11. git rebase -i HEAD~3(last 3 commits calcuated) // It will open 2 text editor one after one, 1st file change 1 squash, 2nd editor create simple one line commit message



