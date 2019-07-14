---
layout: project
title:  "Open World Generation"
date:   2019-05-02 13:42:00
author: Alex Stroud
categories:
- project
img: OpenWorldThumbnail.png
thumb: OpenWorldThumbnail.png
carousel:
- OpenWorld1.png
- OpenWorld2.png
- OpenWorld3.png
- OpenWorld4.png
- OpenWorld5.png
tagged: C++, Programming, Development

---

#### Open World Generation

This project was the second of three tasks under the "Advanced Technologies" module during year three of my degree. The task was to use a dynamic loading system for saving chunks of a game environment and re-loading based on player's distance to each chunk area.


#### Project Summary

The end result of this project was a Unity project that allowed a user to make a custom sized map by setting parameters. As the player moves around the environment, chunks that are out of range will have their information saved externally to a file before being removed from the scene. When the player moves back within range of this area, the system will find the corresponding chunk and load it back from file. This was extended to allow for models on top of each chunk to also be included in the saved information. This means that of the random building type prefabs, they can all be loaded back on top of a chunk they were originally on top of.

After testing, this system is shown to significantly improve the performance conditions of the world when compared to the same project without the dynamic loading being used.

To read about this project further, please follow the link below to find the project report.


#### Report Download Link
[![Open World Report Download](https://i.gyazo.com/64720bd2d83209f573aa646c8ed7a339.png)](https://drive.google.com/open?id=1bnLnOH-5u8POP6n7cIq2kkiynpZTboDd "Report PDF")

#### Building Generator Demonstration Video: Youtube Video
[![CTP Trailer](https://img.youtube.com/vi/cFXJSyragb4/0.jpg)](https://youtu.be/cFXJSyragb4 "CTP Trailer")



