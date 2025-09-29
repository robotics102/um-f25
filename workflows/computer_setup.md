---
layout: page
parent: Workflows
title: Computer Setup
nav_order: 1
---

# Computer Setup

This page contains instructions for installing software needed for ROB 102.

## Command Line Setup

If your computer is running Windows or MacOS follow the corresponding guide below. 

- [Windows Command Line Setup](https://eecs280staff.github.io/tutorials/setup_wsl.html)
- [MacOS Command Line Setup](https://eecs280staff.github.io/tutorials/setup_macos.html)

If your computer is running Linux, simply search for the terminal application, and you should be all set.

## Command Line Usage

To familiarize yourself with using a terminal, you may find [this tutorial](https://eecs280staff.github.io/tutorials/cli.html) helpful. We will go over the basics in lab, so don't worry if it's a little overwhelming. It's perfectly okay to ask for help using the terminal in this course.

## VSCode Installation

Follow the corresponding guide below, based on your operating system. **Only complete steps up to the "Create a project section"!** You won't need the rest for this course.

- [Windows VSCode Installation](https://eecs280staff.github.io/tutorials/setup_vscode_wsl.html)
- [MacOS VSCode Installation](https://eecs280staff.github.io/tutorials/setup_vscode_macos.html)
- [Linux VSCode Installation](https://eecs280staff.github.io/tutorials/setup_vscode.html) - The section under "Linux".

## ROB 102 Specific Extensions and Dependency Installation

Open VSCode, and make sure to connect to WSL if you're on Windows. Then open a new terminal by clicking ```Terminal``` then ```New Terminal```. In the new terminal run the following commands based on your operating system.

- **Windows:** ```sudo apt update && sudo apt install cmake libgtest-dev```.
- **Mac OS:** ```brew install cmake googletest```.
- **Linux:** ```sudo apt update && sudo apt install cmake libgtest-dev```.

Finally install two more VSCode extensions by searching in the extensions bar. 

- Search for and install the CMake Tools extension by Microsoft.
- Search for and install the Remote - SSH extension by Microsoft.

## Setting Up A Project

In this course we'll rely on the CMake Tools extension to make sure VSCode can understand your code structure properly. This will help tools like the visual debugger to give you more accurate warnings while you are coding. 

- Download project code from one of the project pages on this website. For example, [follow this](https://robotics102.org/um-f25/project_0/#getting-your-code) for Project 0.
- Open the folder with this project in VSCode.
- Click on the CMake extension in the left bar of the VSCode window.
- Under the "Folder" drop down, make sure the project's root directory is selected.
- Under the "Configure" drop down, make sure the first item shows "GCC" with some version information after it. If it shows a different option, edit it and select one of the options beginning with "GCC". 

From here you should be able to build, run, and test your code in your VSCode terminal using commands in each project specification.

Note that we won't rely on the extension for configuring or building code. Each project will have instructions on how to build your code by running commands in the terminal. If you would like to learn how to use the CMake extension on your own, feel free. However, we believe learning to use CMake via the terminal will be a more valuable skill in the long run. 
