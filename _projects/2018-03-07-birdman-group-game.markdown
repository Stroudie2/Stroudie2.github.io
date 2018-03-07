---
layout: project
title:  "BIRDMAN GROUP GAME"
date:   2018-03-05 12:00:00
author: Alex Stroud
categories:
- project
img: BirdmanThumbnail.png
thumb: BirdmanThumbnail.png
carousel:
- Birdman1.png
- Birdman2.png
- Birdman3.png
- Birdman4.png
- Birdman5.png
- Birdman6.png
- Birdman7.png
tagged: C++, Programming, Development, Team

---

#### Birdman Group Game

This is the third 2D game that I have made inside of the ASGE C++ framework. For this assignment, we were put into groups and were asked to develop a game based on the loose concept of the movie "Birdman or (The Unexpected Virtue of Ignorance)". Given that this film is difficult to find a solid theme for, we were given the freedom to make the game styled however we want as long as there was some link back to the film. Our group decided to focus on the scene of the movie where Riggan is found locked out of the theatre without his clothes and has to make his way back. We ran with this idea and decided to make a stealth based game where you have to find your clothes and get back to the theatre without being seen.


#### Gameplay Features

The game features a randomly generated AI, pathfinding AI figures and pixel based movement around the map as opposed to the previous games I have made, whereby everything moved in cells. There are lots of obstacles placed around the map and the player can interact with these in order to hide inside to avoid the AI.


#### Development

This was by far the biggest of the programming projects I have worked on so far. There was a lot we wanted to do with the game and so there was a lot of work to be done. We split up the tasks whereby I did the work for the environment and how the player can work in pixels along it, with a camera-like system in place that allows you to constantly see the character in the middle of the screen, unless you are up against a side or in a corner. In this case, the camera will stay looking in the middle of the screen, with the player able to move away from the centre. This created a really nice looking effect in the gameplay. One of the other team members worked on the AI and the other worked on the player class and artwork for menu screens. I worked out the environment so that there were several different building types including: buildings, bins, manholes and bushes. The buildings were randomly sized between set value for a more realistic city look, and the bushes were worked out so that they could be drawn in lines of more than one. All of the obstacles had interaction in place so that the player could hide from the AI that was to be added in. The buildings, bins and bushes blocked the player from moving through them, but all except the buildings could be used as hiding spots. This required me having different sprites available in each obstacle position that could be changed out when hiding. I also had to make it so that the player would disappear from where they were currently standing so it appears they are in the obstacle itself. I am very happy with how these gameplay elements ended up working out and I am looking forward to the next team project.
