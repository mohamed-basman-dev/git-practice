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
4. command git config --global --list ( For checking the datas whether stored corrrectly or not)
# Create directory in local
1. open terminal or git bash
2. Place the directory as per your need e.g /c/Users/username/ GitPractice  
3. command mkdir dir_name e.g mkdir practice 
4. command cd dir_name e.g cd practice 
# Repository creation
1. Create repository in remote e.g git-practice
2. Copy the repo link
# Clone the remote repository
1. command git clone Repo link
2. command ls - to check the list of files in pwd and whethere it's correctly created or not
3. command echo " To check stages of git, pull and push between local and remote" >> demo.txt - create sample text file
4. command git status - to check stage of file 
5. command git add demo.txt - to list the file in staging/ index to be commited
6. command git commit -m "short message desc" - the list files in staging area will be commited and stored in local git repo
7. command push origin main/master - to push the changes to remote *** First time it will ask authentication
8. go to remote page and refresh the page, then it will be updated


