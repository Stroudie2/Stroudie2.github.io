---
layout: post
title: Snake Progress
date: 2017-11-01T00:32:00.000Z
author: Alex Stroud
categories:
  - Snake Game
  - Low-Level Programming
img: snake-game.jpg
thumb: snake-game.jpg
published: true
---

<b>Snake Game Progress</b>
I have nearly finished the core loop of the snake game and am currently in the process of getting my sprites to display inside the ASGE before adding the finishing touch of movement. I have several different classes that helps separate out the project into specific areas. There is a snake class and a class for the snake segments. Each segment piece will hold several types of details including it's own current direction it's facing in, the type of piece it is (Head, body or tail), and details of what segment is in front of it and behind it to help it with moving around corners. This is done through the use of pointers for each segment that get passed to the next one along so that each one will know the details of the segment in front of itself. This means that then each segment will be able to work out how it has to reposition itself in accordance with the position and other details of the segment in front.

Currently I am having a few issues with the engine in trying to get objects to actually display. However I believe that once I've sorted this issue, it should be easy to just implement in the movement for the snake. Below you can see the pseudocode for some of the functions I have already created.

<b>Setting up the border</b>
This is the general pseudo for how the game will set up the border around where the game is played. For each of the positions, it will assign an enum value that will later be assigned to the correct sprite.
```C++
for loop from i=1 to height-2 (down the rows excluding corners)
{
	(0,i) =  Pipe_vertical
	(width-1,i) = Pipe_vertical
}
for loop from j=1 to width-2 (across the columns excluding corners)
{
	(i,0) = Pipe_horizontal
	(i,height-1) = Pipe_horizontal 
}
left top corner -(0,0) = top left sprite 
right top corner - (width-1,0) = top right sprite
left bottom corner - (0, height-1) = bot left sprite
right bottom corner - (width-1,height-1) = bot right sprite
```


