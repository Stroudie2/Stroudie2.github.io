---
layout: post
title: Snake Progress
date: 2017-11-08T22:32:00.000Z
author: Alex Stroud
categories:
  - Snake Game
  - Low-Level Programming
img: snake-game.jpg
thumb: snake-game.jpg
published: true
---

The first portfolio game, "Snake" has now been completed. I am quite happy with the end result of this project, although it didn't go as well as I had expected. The main problems experienced with this came from the fact that it was a new framework that I hadn't used before.
Planning out the project was going quite well, and I didn't receive too many problems until later on into development, after I'd already set up most of the structure of how the code was going to work. However, after I'd implemented the code for creating the board and some other bits of setup, I wanted to try get something displaying before I moved onto the gameplay aspects of the snake moving. This is where I fell behind with the project. I wanted to try and have the rendering working in the individual classes of code, to make it more object oriented. But it took a long time to discover how to access the renderer in files that weren't the core source file. By the time I managed to find how to do it, through looking at the other project "DungeonDeath", I didn't have much time left to finish the game. This meant that in the end I didn't manage to fully implement everything I wanted to. I had the game running and working before I tried to implement a menu system that would allow the player to change settings, have a game over screen etc. This was going to use different game states that would set up the scenes based on what state you were in. I added in all of the code for this, but it didn't seem to be displaying anything and just didn't work. I eventually took it out and added some final changes to the main gameplay before trying to re-implement the menu near to the end of the project. This was unsuccessful and ended causing runtime errors everytime I tried. This was dissapointing because as far as I could see, the system should have been working. I put in debug messages in places to make sure it was running through the menu, and it was getting into the main menu scene, but just wasn't displaying.

Overall I didn't manage to get as much done for this game as I had hoped, but I still have a full functioning core game that displays the score for a player. At least for the second project, I will now be better prepared for getting it setup as I now know how to properly access things like the renderer in different classes.
