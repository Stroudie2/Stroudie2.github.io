---
layout: post
title: Snake Segment Class Planning
date: 2017-10-18T00:32:00.000Z
author: Alex Stroud
categories:
  - Snake Game
  - Low-Level Programming
img: snake-game.jpg
thumb: snake-game.jpg
published: true
---

<b>Snake Game First Class Plan</b>
This is my plan for one of the core classes I will be using in the snake game. The segment class which will be responsible for the snake behaviour and updating of length. It includes plans for different enum types to help with sprite creation and for technical ideas of how to update the snake.


<b>Enum Types</b>
Segment type - head, body or tail
Direction - up, down, left or right

<b>Class Variables</b>
local x and y co-ordinates

<b>Plan for class</b>
The first idea I have is that there will be a pointer for checking the segment in front of the current piece, and a pointer for the piece behind. The pointer for the piece in front will hold the segment type and direction which will be used for updating where the current piece will be on the next frame. It will therefore know what sprite to use when it updates to it's next position. The pointer for the segment behind will be used to run through the while loop that updates each segment. It will know it has reached the end of the snake when it reaches a nullptr for the end.

Adding onto the snake will occur one frame after the food has actually been eaten. This is because there could be a problem with doing it immediately. If you were going up a wall and you turn away from that and keep moving till you grab a piece of food, if the tail of the snake is then touching the wall piece it is going to add on and hit into the wall. Therefore by waiting one frame before adding the piece to the snake, it will stop the chance of this happening completely. There may only be a slight chance of this happening during gameplay, but it is better to eliminate anything that could ruin the gameplay experience for the player. For this to work, there will need to be a variable that checks whether a piece needs to be added to the snake or not.

<b>Possible Gameplay Additions</b>
One potential change I could add would be that the snake gets longer automatically over time if food is not eaten quick enough. The speed at which this happens could be set by the difficulty the game is running in.
Other additions I though of are for the food specifically. The food could change in size based on the difficulty playing on. For example, if you were on the easy difficulty then the food could be bigger making it easier to reach. I could also make it so that the food dissapears after time which could be indicated as about to happen by the snake segments flashing. This gives the player incentive to reach the food as quickly as possible.
