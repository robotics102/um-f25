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

All code other than that in the planning in michigan folder is code for the main project. The folders are organized as follows:

- ```/build``` the folder for your build artifacts. Run executables and CTest here.
- ```/data``` files defining input maps and graphs to be loaded.
- ```/include``` header files for defining and documenting graph structures, graph functions, search functions, and utilities.
- ```/scripts``` Python scripts for dealing with maps. (You won't need to use these, unless you're making your own test map.)
- ```/src``` the source files for implementing graph structures, graph functions, search functions, and utilities.
- ```/test``` the source files for the public tests, built into an executable that can be run by CTest.

The first main feature of the codebase is to define a ```GridGraph``` struct that is similar to the ```Graph``` struct from before. The ```GridGraph``` is special because it is a graph that is designed to be initialized from a map built by the SLAM system. The map is a 2D grid of cells. Each cell stores an estimate of the "log likelihood of occupancy" as a signed 8 bit integer. If the cell almost certainly has no obstacles in it, it will have a value close to -128. If the cell almost certainly has an obstacle in it, it will have a value close to 127. If we pick a number between -128 and 127 as a cutoff, we can call all cells below unnoccupied and all cells above occupied. Storing this map as a graph with nodes for each cell and connections between each of the neighboring eight cells, we now have a graph that we can search over to find a path. This definition can be found in ```include/utils/graph_utils.h```. Also in this file, are several functions for working with the graph, some of which you will implement.

The next main feature of the codebase is to define search algorithms on the graph. These will be functions that will take a starting location, goal location, and a graph struct, and then return a path on the graph struct. You will only be required to implement ```breadthFirstSearch()```. These functions are declared in ```include/graph_search/graph_search.h``` and need to be implemented in ```src/graph_search/graph_search.cpp```.

During the implementation of these algorithms you will need to check whether a node in the graph is in collision before deciding whether to search over it. There are two functions for doing this, only one of which will work by default. The function ```checkCollision()``` is given in ```graph_utils.cpp``` and will work without modification. The function ```checkCollisionFast()``` is given, but will only work if a distance transform function is called before. Distance transform functions are only necessary to implement if you want to use ```checkCollisionFast()```, which is not required. 

## Expected Behavior

The expected behavior of each function and the expected usage of each struct should be apparent by the comments in the header files. Please take your time to read over the codebase to get a sense of how the code fits together. 

There are two important points to emphasize for the implmentation of breadth first search:
- The ```getNeighbors()``` function must return neighbors in the order specified in the comment above its declaration. 
- The ```breadthFirstSearch()``` function should update the parent of the current cell if one of the newly visited adjacent cells provides a shorter path back to the starting cell. 

The test cases are designed to expect this behavior, and check it.

## Testing

The functions ```findNeighbors()``` and ```breadthFirstSearch()``` can be tested with ```ctest --output-on-failure``` in the ```/build``` directory.

It is highly encouraged to debug your code by running ```./nav_cli``` in the ```build``` directory. This will ask for an input map file. Provide the file as ```../data/MAP_NAME.map``` for one of the given maps in the ```/data``` folder. The executable will output a ```out.planner``` file with the path you planned. Upload the map and the planner file to the [navigation webapp](https://hellorob.org/nav-app/) to visualize your plan, which is extra helpful for debugging.

Once you are convinced ```breadthFirstSearch()``` is working, you are ready to test on the robot. Make sure you have followed the [Setting Up a Repository](https://robotics102.org/um-f25/workflows/setting_up_repo.html) guide and have cloned an updated version of your code onto the robot. Next complete the following on your robot.
- Navigate to the root directory of your project code with ```cd```.
- Configure your code with ```cmake -B build -DMBOT=ON```.
- Build your code with ```cmake --build build```.
- Move into the build directory ```cd build```.
- Run ```./robot_plan_path```.
