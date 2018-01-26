---
layout: project
title:  "MINESWEEPER C++ GAME"
date:   2017-02-16 14:00:00
author: Alex Stroud
categories:
- project
img: MinesweeperThumbnail.png
thumb: MinesweeperThumbnail.png
carousel:
- Minesweeper1.png
- Minesweeper2.png
- Minesweeper3.png
tagged: C++, Programming, Development, Games

---

#### Minesweeper assignment
This is the second programming assignment I did in the first year of my course. It involved using C++ to produce a console version of the popular game MineSweeper.



#### The gameplay
The most basic task for this assignment was to have it so that you could simply dig specific areas and see how many mines were next to this location. There were also two boost tasks of which, I completed both of. These were to have a timer that would count up every time a new move was performed and also created an auto-uncover ability, like in the real Minesweeper. This meant that when you dug in an area with no mines nearby, it would uncover a large area up to the closest mines. Figuring out how to perform this took a lot of thinking. I had it so that when one cell is dug, the program would search all eight cells surrounding that for a mine closeby, if none were found, it would search the cells surrounding each one until a cell adjacent to a mine had been found. This proved to be very effective with the gameplay and worked much like the original version of Minesweeper.
