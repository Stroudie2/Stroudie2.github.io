---
layout: post
title: Endless Runner First Game Planning
date: 2017-11-19T14:40:00.000Z
author: Alex Stroud
categories:
  - Endless Runner
  - Low-Level Programming
img: commandervideo.jpg
thumb: commandervideo.jpg
published: true
---

<b>Endless Runner First Brainstorming</b>

This is the second game to be made in the ASGE framework. Much like the snake game, it will require different classes for controlling the different aspects of the gameplay. I did a good job in Snake of managing to spread out the game into several classes. The problem I had was trying to get access to the renderer where needed. However, after completing Snake, I am now aware of how to get around this issue.

The endless runner is going to be quite different in how it works. I need to understand Procedural Level Generation and how to have it run throughout the gameplay. This makes me think that there will be a class dedicated to generating the environment. This will have to constantly run whilst the game is playing so that there continues to be more environment to play in. The generation of the environment will happen randomly off of the screen space, and as it is made, will then be moved into the window view. So it starts the generation off-screen and moves it to where it can be seen.

<b>Gameplay</b>
I think for the runner I am going to have a classic running to the right style gameplay, but with some interesting additions to the gameplay, as mentioned below. The movement in the game will be automatic and the player will likely control only the ability to jump over obstacles in the way. There will be collectables to grab and the score will consist of the distance travelled with bonuses from the collectables.

<b>Vectors</b>

Unlike with previous projects, I have now started learning about the use of Vectors instead of dynamic arrays. Vectors are really great becuase they handle the memory management of your software for you. This means that I don't have to worry about using new and delete so much, which will be a great help. Vectors work in the same way as dynamic arrays, just without the user controlled memory management. They also have their own built in functions that allow you to place elements into the array and resize whenever needed, as opposed to normal arrays that have a fixed size and need to be reinstantiated when resized. This should make it much easier to control what is happening for any places where I need an array.

<b>Possible Game Additions</b>

Different types of obstacles, powers that can affect the game


<b>First work</b>
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/blog/InfiniteRunnerEnvironment.jpg">
As you can see from the above image, I have come up with a basic idea of how the environment generation will work.
There will be a variable holding the current height of the floor piece. When spawning a new column of environment, it will use this value and randomly choose which type of piece to use from an enum class holding environment values. Once it has chosen, if it is an incline or decline piece, then it will adjust the floor_height variable accordingly. It then needs to fill the space between this value and the ceiling with blanks or obstacles. After it has filled in the column, it will then move the environment into the displayed area.
