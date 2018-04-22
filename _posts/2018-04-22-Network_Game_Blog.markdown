---
layout: post
title: Crusade Group Game
date: 2018-04-22T17:44:00.000Z
author: Alex Stroud
categories:
  - Networking Game
  - Low-Level Programming
  - Group work
img: Crusade2.png
thumb: Crusade2.png
published: true
---

<b>Crusade progress</b>

This is the final game of the yera to be made in the ASGE C++ framework and is the second to be done as part of a group. The difference with this one is that it requires the use of a networking library to allow two different clients to play together in a turn based combat game using a server to send data between the clients.
We started off by planning what sort of game we wanted to make and decided to go with an old fashioned turn-based game whereby for each player, they can use one move for all of their five characters before ending their turn. The game mixes the turn based combat with a sort of chess-like gameplay in the way that different characters have movement / attack ranges which are all different sizes. This means that some characters can hit enemies from further away, and others will have to be much closer to their target.
As the game is two-player, the data from characters moving and attacking has to be sent between the two clients for them to locally display what has happened.

<b>My progress</b>
My own work on this project was more towards the setup of the game board components and the actual gameplay of how all of the states would work together when different click combinations have been made. This 
