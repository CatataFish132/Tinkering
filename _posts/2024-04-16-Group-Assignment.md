---
title: "Group Assignment: Logic Blocks"
date: 2024-04-16 11:36:37 +0100
categories:
  - Assignments
tags:
  - week-8
toc: false
math: false
pin: false
comments: false
mermaid: false
img_path: /assets/posts/logicblocks
image:
  path: preview.jpg
---
# Introduction

The group assignment was to start with a specific Electrical Engineering related scope and to find technical hurdles that prevent tinkerability. Once the technical hurdles were found we had to solve them using a material (re)design. We started with finding 2 technical hurdles, thought of 2 concept designs that could overcome that hurdle and finally chose one of the designs we came up with to elaborate on. We created a playground session for the chosen design and also made some prototypes and scaffolding materials for it.

# 2 Problems

The first problem we came up with and wanted to solve was the connectivity of digital electronics. When you want to work with digital electronics, it will mostly end up in a mess of wires that isn't comprehensible at all. Each of the individual gates also need their own power and ground provided alongside the signal. If the wires are connected in the wrong way you might even destroy the gate itself. These are all bad characteristics for tinkering.

Another problem we came up with was that it is hard to get started using an Arduino. Sometimes you want to make a small project that requires programming, but you don't want to learn programming, well how do you do that?

# 2 Ideas

The idea we came up to solve the first problem was Logic Blocks, these blocks with the digital logic inside that could be easily connected/chained to create combinational logic. Each block is quite self explanatory, the left side has the inputs and the right side the outputs. The initial idea was to use AUX cables to connect each block together, this is because 2 channel AUX has 3 wires which can be used for ground, power and signal. This would make sure it is impossible to connect the blocks in the wrong way making it idiot proof, and it is easy to plug in and undo.

To solve the second problem, we came up with an idea to integrate AI into the official Arduino IDE, this helper could write for you but also detect errors, check syntax, and more. So it is not only useful when you don't want to program at all, but it can also help when you decide to learn to program.
# Pitches

We had to present these 2 problems in very small pitches to the class. It was made quite clear by the class that the first idea was the better one of the 2 and that is also the one we pursued. The feedback we got was that the ceiling was a bit low, so instead of only doing combinational logic, we decided to also make it so that the idea itself could be used to make state machines and even processors.

# Design

 The basic gates all have the inputs on the left and outputs on the right. We switched from AUX to a JST connector because these were easier to obtain and cheaper. The electronics in the gates we made from transistors, diodes and some resistors. I wanted to use IC's but these were hard to get at the UT and they very often come with multiple gates in one IC which we didn't need.

# Prototyping/Realization

## Paper

![Desktop View](paper.jpg)
Our design journey started by first making a proof of concept on paper. The goal we set for ourselves was that we should be able to make a 1 bit full adder with the blocks we made. We made the blocks out of paper and glued them to a bigger piece of paper and drew the lines that would be the physical connections of our actual block later. Doing this we found out we were actually missing a very important block, the splitter block. After making some splitter blocks we were able to create the 1 full bit adder and we moved onto the next step.

## 3D design

![Desktop View](block.jpg)

I made the 3D model for the gates. Each gate is modeled after an and gate and is clearly labeled. The blocks themselves are 3D printed by the creality cr-20 I have at home. The black filament ran out after some so we switched to white because it was the only one I had left. A problem we faced was that the holes were too little so I redesigned it.

## Electronics

![Desktop View](electronics.jpg)

We made the logic gate circuits using diodes, resistors and transistors. Firstly we looked up the circuits online and recreated them in kicad. After understanding how they work we created the circuits in a breadboard and tested them. Lastly we made the circuits in some protoboard, soldered all of them and the JST connectors to them, and did the tests for the last time.

# Playground

Our playground session is an introduction to digital electronics using our Logic Blocks. It is meant as an introduction to digital electronics so the main goal is learning. More information about the playground can be found [here](/posts/session-4-reflection).

## Scaffolding

![Desktop View](scaffolding.jpg)

We designed some cards that are used for scaffolding. There are some cards that are already filled in fully like the full/half adder and the decoder card. Cards for the basic gates are not filled in and should be filled in by the user themselves. There are also some karnaugh map cards that are super handy and every digital electronics student should have them.

# Discussion
The final prototype we made was a good proof of concept but it still has some problems. Wires are still kind of a mess but it is more organized than just using a breadboard, this can be fixed by shielding the 3 wires together or using an AUX cable instead of JST. A separate input and output block is needed instead of the breadboards we used. I really like the scaffolding cards we made and I'm proud that the final design worked quite well even though it was a bit janky.