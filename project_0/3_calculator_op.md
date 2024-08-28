---
layout: page
parent: Project 0
title: Calculator Operation
nav_order: 3
---

# Calculator Operation
{: .no_toc }
Project 0 Activity
{: .fs-6 .fw-300 }

## Instructions

In this activity you'll implement a program to collect two operands from the user and act on them with an operator supplied by the user. Complete the following:

- Write a program in ```src/5_calc_op.cpp``` so it performs the behavior specified below.

Just a reminder that ```std::cin >> my_variable``` will attempt to convert input text to a numeric value if ```my_variable``` is a number. 

- *Hint: Mind the formatting!!!*

## Expected Behavior

This checkpoint assumes a potentially adversarial user who might not always enter values that directly adhere to the prompts. The user may enter incorrect values for operands, but will not type spaces and will not type more than one character for an operand. The user also always enters numbers correctly. Lucky you! The prompts should run as follows:

Program:
```
Please type a number and press enter: 
```

User:
```
<response 1>
```

Program:
```
Please type a math operator (one of: + - * or /): 
```

User:
```
<response 2>
```

Program:
```
Please type another number and press enter: 
```

User:
```
<response 3>
```

At this point three things can happen depending on what the user entered. If the user has attempted to divide by zero, the program should output the below to stderr and return -1.

```
Error: Divide by zero attempted!!!

```

If the operand is not one of the four options given in the prompt the program should output the below to stderr and return -1.

```
Error: specified operation (<response 2>) not recognized.

```

Otherwise (if the operand is valid and there is no division by zero) the program should output the result of the operation and return 0.

```
Here's the result of the operation!
<response 1> <response 2> <response 3> = RESULT_OF_THE_OPERATION

```

Make sure to use ```float``` type variables to represent the operands. And finally, make sure to follow the formatting shown here down to the character!

## Testing

All the code for this checkpoint can be tested by running the local unit tests. Make sure your code is built first. Then run ```ctest -R CalcOp --output-on-failure``` in the ```/build``` directory to test only the code for this checkpoint.

If you're rusty on your arithmetic or trying to figure out which character you left out you can run your program with ```./calc_op``` in the ```build``` directory.