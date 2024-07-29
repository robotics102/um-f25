---
layout: page
parent: Project 1
title: Follow Me 1D
nav_order: 2
---

# Follow Me 1D
{: .no_toc }
Project 1 Checkpoint
{: .fs-6 .fw-300 }

## Instructions

In this checkpoint you will implement bang-bang control and p-control and then use them to control the robot in one direction. You'll use these feedback controllers across many parts of projects 1 and 2. First implement the feedback controllers such that they pass the unit tests. Then implement follow me 1D. Complete the following:

- Implement ```bangBangControl()``` in ```mbot_lib/mbot_lib/controllers.cpp``` according to the header file ```mbot_lib/mbot_lib/controllers.h```.
- Implement ```pControl()``` in ```mbot_lib/mbot_lib/controllers.cpp``` according to the header file ```mbot_lib/mbot_lib/controllers.h```.
- Implement follow me 1D in ```p1_wall_follower/2_follow_1d.cpp``` so that the robot performs the behavior specified below.

Remember to check out the [MBot Bridge API](https://hellorob.org/mbot/bridge-api).

## Testing and Expected Behavior

The functions can be tested by running the local unit tests. 

The robot behavior can be tested by running the ```follow_1d``` executable. The robot should follow an obstacle in the forward/backward (x) direction as shown in the video below.

<iframe style="max-width: 100%;" class="centered" width="560" height="315" src="https://www.youtube.com/embed/Y2b7c88kBR8?si=dsbJL7shes1BAtYB" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe><br/>
