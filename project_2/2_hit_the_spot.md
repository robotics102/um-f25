---
layout: page
parent: Project 2
title: Robot Hits the Spot
nav_order: 2
---

# Robot Hits the Spot
{: .no_toc }
Project 2 Checkpoint - WARNING: THIS MATERIAL IS UNRELEASED AND SUBJECT TO CHANGE!
{: .fs-6 .fw-300 }

## Instructions

In this checkpoint you will implement a function to transform a vector between coordinate frames. You will then implement a function that takes your goal pose in world frame and your current pose in world frame and returns a drive command in robot frame that will move your robot straight toward the goal. You will then use this function to write a program that accurately drives the robot to a specified location in a straight line. Complete the following:

- Implement ```transformVector2D()``` in ```mbot_lib/mbot_lib/utils.cpp``` according to the header file ```mbot_lib/mbot_lib/utils.h```.
- Implement ```computeDriveToPoseCommand()``` in ```mbot_lib/mbot_lib/behaviors.cpp``` according to the header file ```mbot_lib/mbot_lib/behaviors.h```.
- Implement robot hits the spot in ```p2_bug_navigation/2_hit_the_spot.cpp``` such that the robot performs the behavior specified below.

You'll want to use ```transformVector2D()``` in ```computeDriveToPoseCommand()``` and then use ```computeDriveToPoseCommand()``` in implementing hit the spot. 

## Expected Behavior

The terminal should ask for the user to input values for an (x, y, theta) goal pose. The robot should then drive in a straight line to the goal pose. Finally the terminal should output the final odometry position of the robot. The final odometry pose should be very close (within a centimeter and 0.15 radians) to the input goal pose. Be sure to show input goal pose and final pose in your terminal during your demonstration.

## Testing

The function ```transformVector2D()``` can be tested by running the local unit tests. The function ```computeDriveToPoseCommand()``` is not tested and is simply provided to help you structure your code so that it can be reused later in project 2. To test only the functions for this checkpoint run ```ctest -R TransformVector2D --output-on-failure``` in the ```/build``` directory.

The robot behavior can be tested by running the ```hit_the_spot``` executable. 