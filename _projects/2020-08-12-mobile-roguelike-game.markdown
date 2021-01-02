---
layout: project
title:  "Mobile Rogue-Like Game (Currently in Development)"
date:   2020-01-29 15:18:00
author: Alex Stroud
categories:
- project
img: RogueLikeThumbnail.png
thumb: RogueLikeThumbnail.png
carousel:
- Rogue-Like_Gameplay_1.png
- Rogue-Like_Gameplay_PickAbility.png
tagged: C#, Programming, Development, Unity

---
# Contents
1. Differences With This Game
{:toc}

# Mobile Rogue-Like Game (History)

This project revolves around my indepently made mobile game, a currently un-named 'Rogue-Like' game developed in Unity. This project began following a long-running interest in these types of games over the past year. Many different versions of the same rough idea have sprouted out across mobile platforms, and seem to all bring a large following with them. The most popular example of this, is the game 'Archero' standing for 'Archer Hero'. The premise of this game and those like it is as the player you move between several rooms filled with various enemies that attack you. As you move around, you try to dodge the incoming attacks. Standing still however, causes the player to start automatically targeting and attacking the closest enemy to themselves. Once a room is clear, the player is rewarded with in-game exp and they move to the next room. The real minute-to-minute excitement of this comes from the large varierty of abilities obtained throughout your playthrough. Each time the player ranks up, they are given a choice between three random abilities that will effect the rest of their gameplay. These abilities vary from increasing the amount of projectiles the player shoots, to adding various elemental effects when hitting enemies. As well as the in-game abilities, the player can collect a massive variety of equipment that will boost their stats throughout the game, encouraging the player to participate more and more to reach the further levels. It's a very fast paced, hyper-active game that keeps players coming back for more with a free-to-play monetisation system. As a long time player of this game, and those like it, I decided it'd be a really interesting project to develop for my own first public game, and as such, this project was started.


# Differences With This Game

When developing this game, in order to add more variety against other similar games, I researched some of the more specific criticisms fans have of these games. This is particularly easy to understand when following the Reddit for a particular game. Here you will find some of the most enthusiatic fans, and as such, you will see them present their most honest feedback about what makes the game good, and what could make it better. For example, one of the most common critiques I've seen mentioned revolves around the gaining of particular equipment. There are various weapon types that people are accustomed to, and in order to better upgrade these items, a 'fusing' system is in place requiring three of the same item in order to achieve the next rarity level and further improve the stats. With the ever-increasing item pool, and the randomness of obtaining a particular item, it requires a massive amount of game time or 'grinding' in order to have a chance of improving a particular item you're used to. That's why with the game I'm developing, one of the core ideas will be to make specific character types which each have certain equipment sets. When playing through levels, they will only have a chance of dropping items specifically for that character type. This means that players can essentially level various characters separately from one another if they have a particular play-style. I belive this will make a significant improvement with player feedback. I am also planning a much more in-depth customisation system that will allow the player to really customise each of their pieces of equipment through varying attachments, effecting specific stats over others. So if for example, a player wanted their weapon to focus entirely on firing as fast as possible, then they could adjust their item in such a way that increases the attack speed, while reducing it's damage and critical hit chance. This system is not entirely planned out yet, but will hopefully be quite complex in the varierty each player can experience.

# Project Developer Diary Playlist: YouTube
Below you can find the playlist to where I am adding new development updates whenever a large amount of progress on the game has been made
<iframe width="560" height="315" src="https://www.youtube.com/embed/R15glwdrvUc?list=PLX_GO8kUDNQ8lPdlOs0ln2FggPmdwSwM3" frameborder ="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Development Stage

Currently, this game is firmly in the early stages of development. A lot of the core gameplay mechanics through the level are there, but variety in characters, or weapons or enemies is still limited as these are quite big areas to expand on. I am currently in the process of planning out how the main menu scene of the game will operate, which will be where the player controls everything outside of the chapter gameplay relating to character customisation etc. As I continue to work on this project, I will update this page further.

The current state of the menu is going quite well, which you can find a dedicated video to in the playlist below. There are currently multiple menu screens working inluding especially the inventory screen, where a player can 'equip' and upgrade their various obtained equipment through the game. This will cost them from their global coins, which are accumulated through each playt-through of a level.


## Menu
I'd like to now go through the menu scene of my project and explain all the features including some technical implementation.

### Menu Interaction
#### Drag Detection
As a mobile game, the menu scene features several different screens which the user can move between either by selecting one of the buttons at the bottom, or by dragging their finger across the screen. This was the first feature I set up, as I always planned for there to be multiple menus available. After spacing the panels out as children of my canvas component, I created a parent object called 'MenuScreens'. Here, I created a script to detect player drag input and in response, the parent of all the screens would be moved in order to position the relevant menu in the display window. In an 'OnDrag' function, which takes in PointerEventData, the amount the player has dragged in the 'x' axis is calculated.
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_OnDragFunction.png?raw=true">
As we drag, we constantly update the RectTransform's local position to be the starting position minus the amount dragged. This keeps the screen moving with the drag.
In the 'OnEndDrag' function, it calculates the amount dragged as a percentage of the width of a screen panel. If this percentage is more than a set threshold of 50%, a function is called on the 'UIController' to calculate the response. This function calculates the distance between each of the five menu screens and the current anchored position of the parent object. Whichever screen is detected as the closest is the one we will slide the display towards upon releasing the drag detection.
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_CheckDragMovement.png?raw=true">

#### Button Presses
Button presses for the different menus link to a 'ChangeMenu' function in the UIController. In here we detect which button was pressed by casting the integer to it's relevant enum value. 
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_ChangeMenu.png?raw=true">
This will then call the function for that menu screen which moves the parent object into view.

### Inventory Details
Most of the menu screens currently don't contain much data, apart from the inventory menu, which is where most of the work has currently been dedicated to.
#### Refresh Inventory
When we select the inventory menu, we first call an event to refresh our player's inventory. This event is subscribed to a function 'RefreshInventory' on the GameManager object. More about script communication later on. This refresh function goes through an ordered process. It first checks if there are any existing items in the player's inventory to be loaded in. It currently does this by checking a specific folder in the device's persistent data path, under the game save data. We check the number of folders representing unique item IDs and return this to the GameManager.
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_GetNumberOfClassItems.png?raw=true">
If there are any existing items for the player, we add them to a list which is then passed to the sorting function before invoking an event to create the prefabs for these items.
The next step of the refresh process is to determine if any new items have been picked up through playing the game and add these to the current list of items to load. To achieve this, we check the list of enum values stored on the class data Scriptable Object used in-game. For each of these new items we invoke another event to spawn the prefabs for new items.
#### Instantiating Item Prefabs
The two functions for instantiating item prefabs work similarly. One is for existing items and the other is for creating new items for the first time. When creating a new item prefab, we pass in the details of what item type it will be(weapon, armour etc), and the specific item enum. We then instantiate a prefab for the type of item, and create a new scriptable object to hold the data of this specific item. The data file will be used to save all the details of this item between scene changes and when opening and closing the game. Every time a change is made to an item, it'll overwrite the saved data for it. As part of this process, we assign each data file a random id value on creation, which is unique to that specific item. We use this id value in the saving process too.
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_ItemDataID.png?raw=true">
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_Menu_ItemFolderView.png?raw=true">

After creating a new data file for each item, we assign some of the default values based on what we know about the item already. Most of these base values are predefined in a serialised Dictionary in the engine inspector.
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_ItemDictionaryInspector.png?raw=true">
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_ItemDictionaryCode.png?raw=true">
This means that throughout the development process I can easily change values for testing processes which will effect any items I equip.
As well as the data file, we also have to fill in the data we use for serialising the prefab in the game. We assign the data to the script attached to the prefab of the GameObject, which will be used until the inventory is next refreshed. Finally we assign the click event to the button representing the item in the inventory display. This means that when the item is pressed, it will open the ItemOverlay screen and know the data specific to the item pressed.
<img src ="https://github.com/Stroudie2/Stroudie2.github.io/blob/master/assets/img/project/carousel/Rogue-Like_Menu_InventoryMenu.png?raw=true">
The function for existing items works mostly the same. The only difference here is that instead of filling the data file with default data, we fill it with the saved data from this item that already existed before.

### Item Overlay
