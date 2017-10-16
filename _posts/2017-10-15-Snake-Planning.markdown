---
layout: post
title: Snake First Game Planning
date: 2017-10-15T16:24:00.000Z
author: Alex Stroud
categories:
  - Snake Game
  - Low-Level Programming
img: snake-game.jpg
thumb: snake-game.jpg
published: true
---

<b>Snake Game First Brainstorming</b>

The snake game will be made using the ASGE, written in C++. It will require the use of different classes for different aspects of the game such as a class for the snake, a class for the movement of the snake and classes for other core parts. There will need to be positioning variables for the snake including default positions for the game to start on and other such variables as the current size of the snake which will effect the array holding it. The snake will be represented using a dynamic array that will be updated as the score is increased. It will need to allow for the movement across the board in different directions, keeping the back positions of the snake in the correct place until they have also moved along the trail.

The food that appears on the map will have to be calculated to appear in a random spot that is not one of the positions currently taken up by the snake. In order for the snake to show in the correct direction that it is moving, I will need a condition that checks where the tail point of the snake currently is and the direction it is moving in, and it will have to add a new bit onto the correct position with the correct facement.



<b>Arrays</b>

There will be a few different arrays in this game that will represnet different things. There will need to be an array for the empty game board where everything will take place and there will need to be arrays for the different things that could take up co-ordinates on the game board (part of the snake, food, walls, empty movable space). The different options for what a cell may currently be could be done through the use of enums for the different options. So for example, an enum for "cell state" that could include within it the different states a co-ordinate on the board can be in.

<b>Possible Game Additions</b>

Having different levels to the game which may increase in difficulty, having lives, some sort of AI (perhaps in the end game screen there could be an automated version of the snake game playing).
