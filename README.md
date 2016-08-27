# HowToPushEclipseProjectToGitHub
Steps to push the code from Eclipse project to Github repository.


You can do this in different ways.. Here is one way:

<b> I. Create repository in Github: </b>

1) Go to https://github.com

2) Login with your crdentials.

3) In the home page, Click on "New Repository" (displayed in Green color) button.

4) Enter the Repository name. This should be unique repository name in your user directory / for your user name. 
Let us name the repository as "DemoRepo".

5) Enter the description of the Repository. We will call the "Repository" as "Repo" or "repo" going forward.

6) Mark it as Public or Private depending on whom you want to share the repo.

7) Check the checkbox to initialize the repo with a ReadMe.md file. This file used as a decription of the project we are creating or how to use the project or any guide lines / versioning, etc.

8) Click on the "Create Repository" button (displayed in green color).

9) This will take you to "DemoRepo" home page. This repository we created on github is called Remote Repository. 

10) You will see "Clone or download" button in green color on top right hand side. You will also see "Branch: master" on top left hand side. This means, the branch name on the remote repo is called as "master" branch.

Let us click on the "Clone or download" button. This will show the github link which can be copied and used in our next section. Here is the link I got from our github project created:
https://github.com/sksubhani/DemoRepo.git

<b> II. Create the project in Eclipse: </b>

1) In Eclipse IDE, create a project (For Ex: a Java project) and add your code if you want.

2) Open a terminal or command prompt. Go to the location (path) of the project.
For ex: The code is located in "/Users/subhani/Documents/workspace/JavaProject/genericsdemo" path.

3) Run the below commands. A copy of the commands can also be found in below link:
https://help.github.com/enterprise/11.10.340/user/articles/adding-an-existing-project-to-github-using-the-command-line/

 $ git init
 This will initialize local directory as git repository.
 
 $ git add .
 This will add all the files from this Eclipse project to Stage area in for git.
 
 $ git commit -m 'Initial commit'
 This will commit the files which are in the stage area.
 
$ git remote add origin << remote  repository url >>
The "remote repository url" can be obtained from the "Clone or download" button on the repo which is mentioned above (https://github.com/sksubhani/DemoRepo.git)

This will links / hooks the local repository to the remote repository mentioned in the url above. Going forward, whenever we push the code from this local repo, the code will be pushed to the remote repo mentioned at the url above.

$ git remote -v
This will show the remote url we just added for confirmation.

$ git pull
This will pull any latest updats from remote repo to local repo. Execute this command before we push our local repo to remote repo.

If the command opens a pop up to save the remote changes into local, save the changes and close the file.

$ git push origin master
This will push the code from your local repo to remote repo. The "origin" is the name of the branch in your local repo. The "master" is the branch name in remote repo.

With this, you should be able to set up your project in Github which is created in Eclipse.
Note: The project name in the Eclipse need not have the same name in Github. You can use other git commands going forward to pull and push the changes from local and remote repositories.
