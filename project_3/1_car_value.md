---
layout: page
parent: Project 3
title: Car Value Calculator
nav_order: 1
---

# Car Value Calculator
{: .no_toc }
{: .fs-6 .fw-300 }

## Code Setup

This activity will be downloaded and completed as a stand alone file. To get the starter code download the file by clicking [here](https://robotics102.org/um-f25/assets/template_code/car_value.cpp) or running the commands below in your terminal. Note that the easiest way to get the file into WSL on Windows will be by using your terminal. 

* Navigate to a directory where you want to keep this activity.
* Download the files from the website ```wget https://robotics102.org/um-f25/assets/template_code/car_value.cpp```.

Build your code by running ```g++ car_value.cpp -o car_value -std=c++14 -Wall -Werror -Wextra```. Run your code by running ```./car_value```.

## Instructions

In this activity you will get familiar with structs by creating a program for determining the price of a car. Complete the following:

- Implement the marked tasks in ```car_value.cpp```.

## Expected Behavior

The program should prompt the user to enter information about all the data members of the ```Car``` struct. It should then ask for a number of years in the future to estimate the value of the car. It should output the estimated value of the car in the future at least once. To calculate the value, follow the guidelines in the function documentation. 

## Testing

There are no automated tests for this file. A $60,000 Mercedes should cost about $13,388 in 10 years. A $20,000 Subaru should cost about $7358 in 5 years. A $90,000 Tesla should cost about $2,117 in 15 years. 

Clearly we don't know much about cars! Feel free to design a better estimate in your own time :)