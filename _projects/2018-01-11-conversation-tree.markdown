---
layout: project
title:  "Conversation Tree"
date:   2018-01-11 14:00:00
author: Alex Stroud
categories:
- project, Assignment
img: ConversationTreeThumbnail.png
thumb: ConversationTreeThumbnail.png
carousel:
- ConversationTree1.png
- ConversationTree2.png
- ConversationTree3.png
- ConversationTree4.png
- ConversationTree5.png
- ConversationTree6.png
- ConversationTree7.png
- ConversationTree8.png
- ConversationTree9.png
- ConversationTree10.png
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
The other engine that I used in this assignment was the Unity Engine. Unlike Unreal with it's visual scripting 'Blueprints', Unity focuses on using code for all of it's logic in the language of C#. For this engine, I decided that I wanted to do it differently to how I had in Unreal where it was purely UI based. As part of this assignment is showing how the given aspect can be implemented into a wider game, I thought I would make a more interactive level for this example. For this example, I was going to have it so that as the player, you were interacting with an NPC, but based on the outcome of the conversation, this NPC has an 'attack' mode in which it gets angry and starts to chase you around the map. 
