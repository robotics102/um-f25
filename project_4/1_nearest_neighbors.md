---
layout: page
parent: Project 2
title: Nearest Neighbors
nav_order: 4
---

# Part 1: Nearest Neighbors
{: .no_toc }
Project 4
{: .fs-6 .fw-300 }

In Part 1 of this project, you will implement a Nearest Neighbor classifier. The nearest neighbor algorithm takes a test image and finds the closest train image, which we call the image's nearest neighbor. Then, it assigns the test image the same label as its nearest neighbor. Here is an example of some MNIST images and their nearest neighbors:

![Nearest_Neighbor_Outputs](https://robotics102.org/um-f25/assets/images/p4/nearest_neighbor_mnist.png){:style="width:800px;" .centered .rd-corners}

Open the notebook `Nearest Neighbors.ipynb` using the Google Drive link provided, and save a copy in your Drive. The notebook is made up of cells, which can be text cells (in Markdown) or code cells (in Python). You can run a cell by pressing the play button in the top left corner of the cell.

You need to run a cell before you use anything it defines in another cell. For example, you should always run the imports cell when you start the notebook. Similarly, you must run a cell which defines a variable or function before running a cell that uses it. Start by running the import cell at the top of the notebook to import some dependencies we'll need later on.

The text in the notebook contains descriptions of how the data is stored and how distance should be calculated. Places where you need to write code are noted in the comments, with the label TODO. Use the provided test cells to check that your functions are working correctly.

Please read through the notebook carefully to make sure you do not miss any important instructions!