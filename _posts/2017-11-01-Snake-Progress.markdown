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
