---
layout: page
parent: Project 3
title: Planning in Michigan
nav_order: 2
---

# Planning in Michigan (In Code)
{: .no_toc }
{: .fs-6 .fw-300 }

## Instructions

In this checkpoint you will find a path using the Breadth First Search algorithm on a map. You will plan in one of these maps, which is customized based on where you are taking the course:

<div markdown=1 style="text-align: center;">
![DC Metro Map](/assets/images/p3/dc_metro_map.jpg){:style="max-width:400px;"}
![Michigan Map](/assets/images/p3/michigan.png){:style="max-width:400px;"}
</div>

Complete the following:

- Design a way to store node data needed in BFS. Add members to the `Graph` struct to store this data.
- Complete function `initGraph()`. It should create space to store data for each node in the graph and initialize any data you might need.
- Complete function `getParent()`. It should return the index of the parent node. If the node has no parent, it should return -1.
- Complete function `bfs(start, goal, g)`. It should perform Breadth First Search to find a path from node index `start` to `goal` within graph `g`.

### Code Overview

*Coming soon*

## Expected Behavior

*Coming soon*

## Testing

Some of the functions can be tested by running ```ctest --output-on-failure``` in the ```/build``` directory.

To run breadth first search manually, you can run the executable ```./plan_in_michigan``` in the ```/build``` directory. This runs the ```main()``` function in ```src/1_planning_in_michigan/main.cpp``` which is designed to help you see the output of your algorithm.
