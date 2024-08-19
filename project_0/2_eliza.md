---
layout: page
parent: Project 0
title: Eliza 102
nav_order: 2
---

# Eliza 102
{: .no_toc }
Project 0 Checkpoint
{: .fs-6 .fw-300 }

## Instructions

In this checkpoint you'll have a little talk with the user. Complete the following:

- Write a program in ```src/4_eliza.cpp``` so it performs the behavior specified below.

You'll need to output on stdout and take input on stdin.

- *Hint: The line ```std::cin >> my_string;``` reads input until a space, ```std::getline(std::cin, my_string);``` reads input until a newline.*

## Expected Behavior

This program should form a conversation between Eliza and the user. The user can respond however they like, but will only be able to enter one line at a time. Eliza will respond in a very formulaic way. Let's hope you can find a better therapist if you need one. The sequence should proceed as follows:

Eliza:
```
Hello, I am Eliza. I'll be your therapist today.
Tell me, what is your name?

```

User:
```
<response number 1>
```

Eliza:
```
Nice to meet you, <response number 1>, how can I help you today?
What is bothering you?

```

User:
```
<response number 2>
```

Eliza:
```
"<response number 2>"? Please tell me more. How does that make you feel?

```

User:
```
<response number 3>
```

Eliza:
```
Intresting intreseting........ well would you look at the time I am afriad we will have to end the session here.
Have a good rest of your day, <response number 1>, I hope to see you again soon!

```

Here's an example from one of the original developers of the course. This is how the input and output should look together in the terminal window:

```
Hello, I am Eliza. I'll be your therapist today.
Tell me, what is your name?
Jana Pavlasek
Nice to meet you, Jana Pavlasek, how can I help you today?
What is bothering you?
I'm worried the kids in ROB 102 will forget about me
"I'm worried the kids in ROB 102 will forget about me"? Please tell me more. How does that make you feel?
It makes me feel like my years of continued dedication to making this amazing course will be forgotten
Intresting intreseting........ well would you look at the time I am afriad we will have to end the session here.
Have a good rest of your day, Jana Pavlasek, I hope to see you again soon!

```

## Testing 

All the code for this checkpoint can be tested by running the local unit tests. Make sure your code is built first. Then run ```ctest -R Eliza --output-on-failure``` in the ```/build``` directory to test only the code for this checkpoint.

If you want to talk to Eliza on your own run ```./eliza``` in the ```/build``` directory.