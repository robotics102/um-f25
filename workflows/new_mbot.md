---
layout: page
parent: Workflows
title: Getting a New MBot
nav_order: 3
---

# Getting a New MBot

If you've been assigned an MBot for a new project (starting with project 1) there are a few steps you should take to make sure you are set up to code on the new MBot. Follow the steps below.

## Install Dependencies

If you're not the first user of an MBot, the dependencies for this class may already be installed. Read through this section just to make sure.

Connect to your robot via the VSCode remote extension. On the VSCode window for your robot, go to the extensions tab on the left, and look for the CMake Tools extension. If the blue install button says "install on remote" hit the button to install the extension on your MBot. If it says "Uninstall", the extension may have already been installed.

Run ```sudo apt-get install libgtest-dev``` in the terminal on your MBot. You may need to enter the robot's password. The command may say that this package is already installed. This is fine.

## Configure Git and Keys

You'll want to set the global configuration for user and email. You'll also want to generate a new ssh key to authenticate with GitHub on the new robot. To set the user and email run the commands below with appropriate values for ```YOUR_EMAIL``` and ```YOUR_NAME```.

- ```git config --global user.email "YOUR_EMAIL"```
- ```git config --global user.name "YOUR_NAME"```

Follow the [Setting Up a Repository](https://robotics102.org/um-f24/workflows/setting_up_repo.html) guide to set up your project and be sure to generate a new ssh-key on the robot.
