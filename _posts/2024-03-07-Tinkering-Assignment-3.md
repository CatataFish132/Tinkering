---
title: Assignment 3 Programming
date: 2024-03-07 11:28:38 +0100
categories:
  - Tinkering
  - Assignments
tags: 
toc: false
math: false
pin: true
comments: true
mermaid: false
img_path: /assets/posts/programming/
image:
  path: preview.jpg
---

# Assignment 3 Physical Analogy for Programming
I wanted to focus on a few aspects of programming:
- Variables
- Program Flow
- Loops
- If statements

I wanted my idea to have cards and a pawn, the pawn would indicate where the program is currently at and the user has to move the pawn according to what the card says.
My idea was to have a bunch of cards with arrows, the arrows would represent the program flow and on some cards would be actions that would have to be done like i = i+1. If statements would just have different directions for true and false and loops would just loop back to an earlier point.

But to make it more fun so I changed it to a racetrack. Now the race car is where the instruction pointer is at. The signs next to the road would tell the driver what to do. If statements would be junction so the sign might say something like if the variable i is lower than 3, make a right turn. This turn might actually lead back to an earlier road so that's how loops are done.

# Setup
I printed out an A4 paper full of squares approximately 6 by 6 cm, I then drew all the cards I wanted on that paper, these included just a straight section of road, signs, turns and splittings. I then scanned this piece of paper and then cropped out all the squares. After I finished I could print out the squares on paper and cut them out with scissors, this way i didn't have to draw the same square twice and saved me a lot of time.

# Variables
![Desktop View](var.jpg){: .w-50}


For the variables i used spinners, so there would be a sign next to the variable saying what the name is and the spinners would indicated what value the variable has currently. 
# If Statements

| If Else Statement | If Statement       |
| ----------------- | ------------------ |
| ![](if.jpg)       | ![](simple_if.jpg) |


For the if statement a road splitting is used. The sign indicates when you should go right or left depending on the condition that is also written on the sign. So a sign might say something along the lines as "turn right when A>B" This is equivalent to an If statement in programming. In the first image you see an If Else statement, so If A>B then go right Else go straight, there could be some code at the right section of the road but if its empty it will just act as an If statement. So the left would be:` If A>B Do something Else continue` while the left one would be `If B==0 Do something and end, Else do this other thing and end`.

# Loops
![Desktop View](loop.jpg){: .w-50}

This is a loop in this system, the car enters the loop and can only exit when the condition is met, which in this current case is that B\=\=0. This is entirely done with the same cards as the if statements are done with but now it goes back into the road at the end, thus creating a loop.

# Euclidean algorithm
![Desktop View](preview.jpg)

I wanted to make something in this system that would be actually useful. This system in the picture now find the GCD aka Greatest Common Divider. This is done with the euclidean algorithm. First the variables have to be set, in this example I have set A to 48 and B to 18. The car then starts at the left and enters the loop. If A is greater than B it will go to the right, which is true so the car goes to the right and the sign then says to subtract B from A and store it in A. It then drives back to the start. This continues till B is equal to 0, the next round A is still greater than B so it does the same path again but the round after A is smaller than B so it will go continue the road and end up at the sign where it should subtract A from B and store it in B and then drive to the start of the loop again. After a few more round B would be equal to 0 so the car can finally go left at the start of the loop and the final answer will be stored in A which would be 6 in this case.

```python
while b != 0:
	if a > b:
		a = a - b
	else:
		b = b - a
return a
```

