---
layout: page
parent: Project 3
title: Path Planning
nav_order: 3
---

# Path Planning
{: .no_toc }
Project 3
{: .fs-6 .fw-300 }

## Instructions

This is the final checkpoint for the wall follower project. You will implement functionality for a ```GridGraph``` which is a grid shaped graph over which you will search. You will then implement the breadth first search (BFS) search algorithm on this graph. Finally, you will initialize a ```GridGraph``` from your robot's SLAM map, run your algorithm to generate a path, and drive along this path. The code for initializing from the SLAM map and driving along the path is given. Your focus will be on path planning via graph search. Complete the following:

*Graph functionality*
- Implement the ```CellNode``` struct in ```include/utils/graph_utils.h```.
- Modify the ```GridGraph``` struct in ```include/utils/graph_utils.h``` to add a member variable storing information about the graph's nodes.
- Implement the ```initGraph()``` function in ```src/utils/grid_graph.cpp``` according to the header file ```include/utils/graph_utils.h```.
- Implement the ```findNeighbors()``` function in ```src/utils/grid_graph.cpp``` according to the header file ```include/utils/graph_utils.h```.
- Implement the ```getParent()``` function in ```src/utils/grid_graph.cpp``` according to the header file ```include/utils/graph_utils.h```.

*Search functionality*
- Implement the ```breadthFirstSearch()``` function in ```src/graph_search/graph_search.cpp```.

*Running on the robot*
- Call your graph search function and store the result appropriately in ```src/3_robot_plan_path.cpp```. 

### Code Overview

*Coming soon*

## Expected Behavior

*Coming soon*

## Testing

The functions ```findNeighbors()``` and ```breadthFirstSearch()``` can be tested with ```ctest --output-on-failure``` in the ```/build``` directory.

It is highly encouraged to debug your code by running ```./nav_cli``` in the ```build``` directory. This will ask for an input map file. Provide the file as ```../data/MAP_NAME.map``` for one of the given maps in the ```/data``` folder. The executable will output a ```out.planner``` file with the path you planned. Upload the map and the planner file to the [navigation webapp](https://hellorob.org/nav-app/) to visualize your plan, which is extra helpful for debugging.
