---
layout: project
title:  "Conversation Tree Gameplay Aspect"
date:   2018-01-11 14:00:00
author: Alex Stroud
categories:
- project, Assignment
img: ConversationTreeThumbnail.png
thumb: ConversationTreeThumbnail.png
carousel:
- UnrealLevel1.png
- UnrealLevel2.png
- UnrealLevel3.png
tagged: Unreal Engine, Game Engine, Development, Unity Engine, Architecture

---

#### Game Engine Architecture Assignment

This assignment was for my "Game Engine Architecture" module in my second year of my degree and it focused around the use of game engines and how the subset tools that they offer, allow us as developers to make gameplay aspects with great ease when compared to the days before game engines were so common.


#### The Task

This module assignment involved implementing a specific aspect of gameplay or special effect commonly found in games, using different game engines to help. There was a choice of which aspect to choose to implement from: conversation trees, fireworks, cameras or grass. These are all specific sub-systems that can commonly be found in games and so the task was to explore different game engines and identify how they are helpful for implementing the given aspect and how the engines can be used to implement the systems as part of a larger game. I chose to go with the conversation tree as this is a gameplay aspect that I have personally experienced in a lot of the story-driven games that I have played throughout my life. I was curious to research this and find out more about how it works.


#### Unreal Engine

One of the two game engines that I used for this assignment was the Unreal Engine. I already had some experience with Unreal, but not much in terms of UI based worked. I decided after researching the gameplay aspect a bit that I would try to create a visual novel style conversation tree as this was a good way of exploring the key aspect itself. Before actually implementing any of the logic for my Unreal system, I first decided it would be best to plan out how the different text options would link to each other based on the choices made by the user. After writing out the conversation options, I then drew a dialogue scheme, which I had discovered can be the most useful way of planning out a conversation tree. The dialogue scheme shows how different scenes with their different options will link to where they are supposed to go based on the button clicked. Drawing this out first makes it so that when I had to link together the scenes in Unreal, I already knew which order they had to go in by just looking at my diagram.
Implementing into Unreal itself was quite simple. There are lots of useful features that are offered such as an area for storing the text for the conversation inside a structure. This meant that I could then use variables for the specific pieces of text and update them when needed. As you can see from the above images, the logic of the system involves breaking apart the structure, before dragging off the text into their correct places. I knew where the different text options had to go based on my previously mentioned dialogue scheme.


#### Unity Engine
This level was one of the biggest projects I have worked on in the first term of the second year, with lots of planning required to make it enjoyable and playable to the extent of the assignment brief. It was also one of my personal favourite modules to work on as I find the planning and making of different level assets to be a really fun and interesting process.
