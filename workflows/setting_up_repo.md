---
layout: page
parent: Workflows
title: Setting Up a Repository
nav_order: 2
---

# Setting Up a Repository

This is a guide to setting up a git repository in a directory where you want to start a project. Most likely this is the directory containing template code that you just unzipped. Follow the steps below.

## Create a Remote Repository on GitHub

Log into [GitHub](github.com) and follow [this tutorial](https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories) to make a new repository on GitHub. Choose and appropriate name for your repository and **MAKE SURE TO MARK YOUR REPOSITORY AS PRIVATE**. You should end up with a page showing some different commands for setting up a repo. Copy the quickstart link that looks something like ```git@github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git```. You'll need it below.

If you have not already generated an ssh key (if this is your first time cloning a repo on this computer) follow the [tutorial on generating an ssh key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) and then follow the [tutorial on adding an ssh key to your github account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account). You'll need to do this to be able to push to your remote repository.

## Create a Local Repository and Push To the Remote

- Navigate into the directory where you want to make the repository using ```cd```. For template code this is the folder you just unzipped. 
- Initialize a local git repository with ```git init```.
- Name your branch "main" with ```git branch -M main```.
- Add your remote repository to your local repository with ```git remote add origin YOUR_GITHUB_LINK```, where "YOUR_GITHUB_LINK" is the link you copied in the previous section.
- Stage the template code to be committed with ```git add .```.
- Create a commit with ```git commit -m "Add template code"```.
- Push your commit to the remote repository with ```git push --set-upstream origin main```.

If you refresh your remote repository page in your browser on GitHub, you should see the template code.

## Share the Repository With Your Teammate (Teams Only)

If you're working with a partner and you created the repository on your GitHub account, you'll need to give you partner access to the repository. If your partner can already see the repository from their account **Your repository is NOT private**. To add your partner follow [this tutorial](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository).

## Cloning the Repository

You should now be able to create a local repository of your project on any computer that doesn't already have one just by cloning your remote. See the [cloning a repository section](https://hellorob.org/tutorials/git#sec_clone) of the HelloRob tutorial. Note that this guide uses the https link for cloning the repo, while you should copy paste the ssh link (both are options under the green code button on GitHub). 