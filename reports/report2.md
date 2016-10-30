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
Requirements are important because they are one of the key contributors to the success or failure of projects: if what is needed to be done isn't known, we might end up solving the wrong issue entirely.

If we plan software to be high-quality from the beginning, we have a greater chance of it staying that way rather than another product that doesn't have high-quality as a goal.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/Relative_cost_to_fix_an_error.png)

**Fig2 -** Cost of fixing errors depending on the phase of the project they were found ("Software Engineering Economics" book from *Barry Boehm*).

Researchers at big organizations have found that removing an error just before starting to code allows 10 to 100 times less costs than when it's done when testing the system or after release. (Reference: Code Complete 2, TODO: place at end a references section?)

This cost can be explained very simply: if an error is found during the coding stage, it's easy to correct it by fixing a few lines. However, if the error has to do with the overall design of the system, it is much harder to solve, possibly requiring a rewrite of certain features, or even the entire project.

TODO: improve below.

The main problems are:
* (mis)communication
* (mis)understanding

That's why requirements must be as much detailed as possible if we intend to avoid this problems.

##### Requirements Elicitation Process in OpenRCT2
According to developers, OpenRCT2 attempts to provide everything from the original Roller Coaster Tycoon 2, as well as many improvements and additional features. For example, some of these may include support for modern platforms, an improved interface, improved guest and staff AI, more editing tools, increased limits, and cooperative multi player.

When any developer interested in OpenRCT2 has a new idea for the project, the development team recommends contacting them first, since they might already have plans for the same idea, or because the team might have issues against its implementation. By contacting the team, the developer avoids spending time on a feature that might not be accepted. The team can be contacted through [gitter](https://gitter.im/OpenRCT2/OpenRCT2).

## Specific Requirements and Features<a name="specific-requirements"></a>
### Functional requirements<a name="functional-requirements"></a>
#### User requirements<a name="functional-user-requirements"></a>
 * There must be an initial menu that the user can interact with.
 * Pressing the start a new game button in the initial menu must present a dialog with a set of parks to play on, with varying degrees of difficulties.
 * Pressing the load a game button in the initial menu must present a dialog with a list of the saved games that the user can choose to load.
 * Pressing the multi player button must appear a list with the available servers.
 * Pressing the game tools button must present a new window with all the editing tools.
 * Pressing the options button must present a window with the configuration of the game.
 * Moving the mouse through the objects in the game must appear a preview of the object.
 * The game state need to have a little menu at the top right corner.
 * Pressing the demolition button the mouse must be able to take things from the map and must appear a window with the cost of the demolition.
 * Pressing the adjust land button the mouse must be able to change the land height and slove, must appear a window with the cost and size of the land change.
 * Pressing the create and adjust water button a windows must appear with the size of ground for the water and cost and the player must be able to create and change the water in the ground with the mouse.
 * Pressing the place scenery button a windows must appear with all the options do customize the park with a associate cust and the player must be able to put them on the ground with the mouse.
 * Pressing the build footpaths button a new window must appear with the direction, size, type and inclination of the footpaths, and the player must be able to put them on the  with the mouse.
 * Choosing the new attraction button a window must appear to choose the transport ride and the player has to put them on the map with the mouse.
 * Choosing the funding button a window must appear with the progress of the park and the research funding amd priorities.
 * Pressing the guests button, a windows must appear with all the guests of the park.
 * Choosing one of the guests of the guests window, a new window must appear with the information of the guest, like his money, his thoughts, what he is carrying, rides been on and his feelings.
 * Choosing the staff button a new window must appear with all the staff of the park, a option to hire new staff, to fire and to choose the patrolled area.
 * Pressing the park information button a windows must pop-up with all the information of the park such as the status (opened, closed), the park rating, the number of guests, the admission price and the objetives of the player for the park.
 * Pressing the rides in park button a window must appear with all the rides, shops, stalls, toilets and information Kiosks of the park and a option to sort them.
 * While in the game state, the bottom right must have the date of the park, the temperature and weather.
 * In the game state, in the bottom left must appear the total money the player have, the number of guests of the park and the current park rating.
 * Choosing the pause game button, the game state must pause. This includes the atual date.
 * Choosing the change game speed button, the player can choose the speed of the time.
 * Pressing the game options button the player must be able to start a new game, load a previous game, save the game, access to the  options, take screenshots, exit the game and quit to the menu.
 * Pressing the options button on the game options state, a new window must appear so that the player can change the video settings, language, currency, sound settings and controls.
 * Pressing the zoom view the park the player can see the park from a greater distance.
 * Pressing the zoom view the park the player can get closer to the park.
 * Choosing the rotate view 90º button the camera must change 90º clockwise.
 * Pressing the view options button the player can hide parts of the scenery.
 * Pressing the map button, a window must pop-up with the park map see from above.

### Non-Functional requirements<a name="non-functional-requirements"></a>
#### User requirements<a name="non-functional-user-requirements"></a>
* O jogo deve estar optimizado e, por consequência, possuir um número considerável de frames per second;

#### System requirements<a name="non-functional-system-requirements"></a>
* **Processor (CPU):** Pentium III
* **System memory (RAM):** 64 MB
* **Hard disk drive(HDD):** 800MB
* **Video card (GPU):** 8 MB of VRAM, DirectX 8.1 compatible
* **OS:** The game may run in different Operating Systems such as Windows, Unix, MacOS.

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

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/Use_cases_diagram.png)
**Fig3 -** Use cases diagram.

## Domain Model<a name="domain-model"></a>
### Brief Definition
Na engenharia do software, um "domain model" pode ser visto como um modelo conceptual de um sistema que incorpora todas as entidades desse mesmo sistema, a informação e as relações existentes entre estes.
O "domain model" é pois, um conjunto de abstrações que ajudam a entender um dado sistema e a sua atividade.

### Domain Classes
* Park
* Funding
* Scenarios
* Guests
* Staff
    * Handymen
    * Mechanic
    * Security
    * Entertainers
* Attractions
    * Ride
        * Transport Ride
        * Gentle Ride
        * Roller Coaster
        * Thrill Ride
        * Water Ride
    * Shop
    * Stall
    * Toilet
    * Information Kiosks
* ...

**TODO: DOMAIN MODEL**
**Fig4 -** Domain model diagram.

## Contributions
* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

## Bibliography
Use Case explanations: *http://searchsoftwarequality.techtarget.com/definition/use-case*
