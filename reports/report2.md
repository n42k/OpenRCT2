# Report 2: Requirements Elicitation

## Index
1. [Requirements](#requirements)
	1. [Introduction and Description](#intro_descri)
	2. [Purpose/Scope](#purpose/scope)
2. [Specific Requirements and Features](#specific-requirements)
	1. [Functional requirements](#functional-requirements)
		1. [User requirements](#functional-user-requirements)
	2. [Non-Functional requirements](#non-functional-requirements)
		1. [User requirements](#non-functional-user-requirements)
		2. [System requirements](#non-functional-system-requirements)
3. [Use Cases](#use-cases)
4. [Domain Model](#domain-model)

## Requirements <a name="requirements"></a>
### Introduction<a name="introduction"></a>
Requirements are a detailed description of what features a software product should have. They're generally considered to be the first phase of software development.

Requirements are important because they are one of the key contributors to the success or failure of projects: if what is needed to be done isn't known, we might end up solving the wrong issue entirely.

If we plan software to be high-quality from the beginning, we have a greater chance of it staying that way rather than another product that doesn't have high-quality as a goal.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/Relative_cost_to_fix_an_error.png)

**Fig2 -** Cost of fixing errors depending on the phase of the project they were found ("Software Engineering Economics" book from *Barry Boehm*).

Researchers at big organizations have found that removing an error just before starting to code allows 10 to 100 times less costs than when it's done when testing the system or after release. [\[1\]](#reference1)

This cost can be explained very simply: if an error is found during the coding stage, it's easy to correct it by fixing a few lines. However, if the error has to do with the overall design of the system, it is much harder to solve, possibly requiring a rewrite of certain features, or even the entire project.

The time that should be spent on requirements highly depends on the project. If the requirements are stable, it will take less time than if they were unstable. The size of the project is also an important factor: for smaller projects you may be able to afford programming as you create the requirements, whereas that would be very risky in a larger project.

##### Requirements Elicitation Process in OpenRCT2
According to developers, OpenRCT2 attempts to provide everything from the original Roller Coaster Tycoon 2, as well as many improvements and additional features. For example, some of these may include support for modern platforms, an improved interface, improved guest and staff AI, more editing tools, increased limits, and cooperative multi player.

When any developer interested in OpenRCT2 has a new idea for the project, the development team recommends contacting them first, since they might already have plans for the same idea, or because the team might have issues against its implementation. By contacting the team, the developer avoids spending time on a feature that might not be accepted. The team can be contacted through [gitter](https://gitter.im/OpenRCT2/OpenRCT2).

## Specific Requirements and Features<a name="specific-requirements"></a>
### Functional requirements<a name="functional-requirements"></a>
#### User requirements<a name="functional-user-requirements"></a>
 * There must be an initial menu that the user can interact with;
 * Pressing the start a new game button in the initial menu must present a dialog with a set of parks to play on, with varying degrees of difficulties;
 * Pressing the load a game button in the initial menu must present a dialog with a list of the saved games that the user can choose to load;
 * Pressing the multi player button makes a list with the available servers appear;
 * Pressing the game tools button must present a new window with all the editing tools;
 * Pressing the options button must present a window with the configuration of the game;
 * Moving the mouse through the objects in the game must show a small textual description of the object;
 * The game needs to have a menu at the top right corner, with various buttons;
 * Pressing the demolition button the mouse must allow a player to remove objects from the map and must show a window with the cost of demolition;
 * Pressing the adjust land button the mouse must be able to change the land height and slope, a window must appear with the cost and size of the land change;
 * Pressing the create and adjust water button a windows must appear with the size of ground for the water and the cost of construction and the player must be able to create and change the water in the ground with the mouse;
 * Pressing the place scenery button a window must appear with all the options to customize the park using scenery objects with an associated cost and the player must be able to put them on the map with the mouse;
 * Pressing the build footpaths button a new window must appear with the direction, size, type and inclination of the footpaths, and the player must be able to put them on the map with the mouse;
 * Choosing the new attraction button a window must appear to choose the transport ride and the player has to put them on the map with the mouse;
 * Choosing the funding button a window must appear with the progress of the park and the research funding and priorities;
 * Pressing the guests button, a windows must appear with all the guests of the park;
 * Choosing one of the guests on the guests window, the guest information window must appear;
 * The guest information window must show a guest's information, such as his money, his thoughts, what he's carrying, rides he's been on and his feelings;
 * Choosing the staff button a new window must appear with all the staff of the park, a option to hire or fire staff and to choose the patrolled area;
 * Pressing the park information button a window must pop-up with all the information of the park such as the status (opened, closed), the park rating, the number of guests, the admission price and the objectives of the player for the park;
 * Pressing the rides in park button a window must appear with all the rides, shops, stalls, toilets and information kiosks of the park and an option to sort them;
 * While in the game state, the bottom right must have the date of the park, the temperature and the weather;
 * In the game state, the bottom left must show the total money the player has, the number of guests of the park and the current park rating;
 * Clicking the pause game button, the game state must pause; This includes the actual date;
 * Choosing the change game speed button, the player can choose the speed of time;
 * Clicking the game options button the player must be able to start a new game, load a previous game, save the game, access the options menu, take screenshots, exit the game and quit to the main menu;
 * Pressing the options button in the game options, a new window must appear so that the player can change the video settings, language, currency, sound settings and controls;
 * Pressing the zoom out button the player can see the park from a greater distance;
 * Pressing the zoom in button the player can get closer to the park;
 * Clicking the rotate view 90º button the camera must change 90º clockwise;
 * Pressing the view options button the player can hide parts of the scenery;
 * Pressing the map button, a window must pop-up with the park map see from above.

### Non-Functional requirements<a name="non-functional-requirements"></a>
#### User requirements<a name="non-functional-user-requirements"></a>
* The game must be optimized and, as a consequence, meet a set minimum number of frames per second.

#### System requirements<a name="non-functional-system-requirements"></a>
There are no hardware non-functional system requirements in OpenRCT2. However, the original requirements of this type for the original game were:
* **Processor (CPU):** Pentium III
* **System memory (RAM):** 64 MB
* **Hard disk drive(HDD):** 800MB
* **Video card (GPU):** 8 MB of VRAM, DirectX 8.1 compatible

In terms of operating system, however, OpenRCT2 is multi platform and must run in any of the 3 major operating systems (Windows, macOS and Linux).

## Use Cases<a name="use-cases"></a>
### Brief Definition
A use case is a methodology used in system analysis to identify, clarify, and organize system requirements.
The use case is a list of actions or event steps, typically defining the interactions between a role,also know as actor, and a system to achieve a goal.

**Actor -** Actor models a type of role played by an entity, not an individual user of the system, that interacts with the system . Actors are external entities such as people or other systems that interfaces with the developed system.

**Development System -** The software made, it can be an application, a game,etc.

A use case (or set of use cases) has these characteristics:
* Organizes functional requirements.
* Models the goals of system/actor (user) interactions.
* Records paths (called scenarios) from trigger events to goals.
* Is multi-level, so that one use case can use the functionality of another one.

### Use Case Model

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/UC_offline.png).

##### OpenRCT2 Main Menu	
 > **Name:** Main menu.		
 > **Actors:** Older Player,New Player.		
 > **Goal:** The user should see an user-friendly interface.		
 > **Pre-conditions:** None.		
 > **Description:** By starting the game, the main menu is displayed and the user can freely choose between the options given. <br>
 > **Post-conditions:** None.	
 
 ![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/UC_management.png).

##### OpenRCT2 Single Player	
 > **Name:** Single Player.		
 > **Actors:** Player.		
 > **Goal:** The player must try to make a profit and maintain a good park reputation whilst keeping the guests happy.
 > **Pre-conditions:** None.		
 > **Description:** The player starts with a pre-defined park and then he tries to manage everything inside it. <br>
 > **Post-conditions:** Game Won.		

## Domain Model<a name="domain-model"></a>
### Brief Definition
In software engineering, a "domain model" may be seen as a conceptual model of a system that incorporates all its entities and their information, as well as the relations between them.
A "domain model" is, this way, a set of abstractions that help in understanding a given system and its activity.

### Domain Classes
* Park
* Funding
* Scenario
* Guest
* Scenery
* Staff
    * Handymen
    * Mechanic
    * Security
    * Entertainer
* Attraction
    * Ride
        * Transport Ride
        * Gentle Ride
        * Roller Coaster
        * Thrill Ride
        * Water Ride
    * Shop
    * Stall
    * Toilet
    * Information Kiosk
* ...

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/domain_model.png)

**Fig4 -** Domain model diagram.

## Contributions

All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

## Bibliography
[1] McConnell, Steve (June 2004). "Design in Construction". Code Complete (2nd ed.). Microsoft Press. p. 29. ISBN 978-0-7356-1967-8. "Chapter 3: Measure Twice, Cut Once: Upstream Prerequisites" <a name="reference1">

Use Case explanations: *http://searchsoftwarequality.techtarget.com/definition/use-case*
