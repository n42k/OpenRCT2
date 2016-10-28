# Report 2: Requirements Elicitation

## Index
1. [Requirements](#requirements)
	1. [Introduction and Description](#intro_descri)
	2. [Purpose/Scope](#purpose/scope)
2. [Specific Requirements and Features](#specific-requirements)
3. [Use Cases](#use-cases)
4. [Domain Model](#domain-model)

## Requirements <a name="requirements"></a>
### Introduction and Description <a name="intro_descri"></a>
Requirements engineering (RE) is the process of studying custom/user expectations towards a specific product. In other words, requirements engineering means that requirements for a system are defined, managed and tested systematically.
These software requirements deals with establishing the needs of stakeholders that are to be solved by software and fully describes what software will do and how it will be expected to perform.
Requirements must be quantifiable, detailed and not ambiguous.

##### Requirements Elicitation Process 
![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/requirement_elicitation.png)

**Fig1-** Requirements Elicitation Process by "TutorialsPoint".

* Requirements gathering - The contributors discuss with the main developers and know their expectations from the software.
* Organizing Requirements - The contributors prioritize and arrange the requirements in order of importance, urgency and convenience.
* Negotiation & discussion - If requirements are ambiguous, contributors must discuss with main developers to have additional information and requirements be as much detailed as possible.

### Purpose/Scope <a name="purpose/scope"></a>
According to developers, openRCT2 attempts to provide everything from RollerCoaster Tycoon 2 as well as many improvements and additional features. For example, some of these may include support for modern platforms, an improved interface, improved guest and staff AI, more editing tools, increased limits, and cooperative multiplayer.

Sempre que existam por parte de colaboradores, novas ideias para o projeto, a equipa aconselha a contacta-la primeiro, porque podem já existir planos para a sua realização, ou então, porque a equipa pode já ter motivos contra a sua implementação. Ao contactar a equipa, o colaborador evita perder tempo implementando uma feature que pode não ser aceite. É possível contactar a equipa através do [gitter](https://gitter.im/OpenRCT2/OpenRCT2).

### Importance of RE
Requirements engineering (RE) is one of the most crucial sector in Software engineering and can influence the entire software development cycle, because errors produced at this stage, if weren't prevented or fixed, have the highest cost to fix later on. 

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/Errors cost.png)

**Fig2-** Cost of fixing errors depending on the time elapsed.

The main problems are:
* (mis)communication
* (mis)understanding

That's why requirements must be as much detailed as possible if we intend to avoid this problems.

## Specific Requirements and Features<a name="specific-requirements"></a>
### Functional requirements
#### User requirements
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
 * Chossing the staff button a new window must appear with all the staff of the park, a option to hire new staff, to fire and to choose the patrolled area.
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
 * Pressing the map button a window must pop-up with the park map see from above.

### Non-Functional requirements
#### User requirements
* O jogo deve estar optimizado e, por consequência, possuir um número considerável de frames per second;

#### System requirements
* **Processor (CPU):** Pentium III
* **System memory (RAM):** 64 MB
* **Hard disk drive(HDD):** 800MB
* **Video card (GPU):** 8 MB of VRAM, DirectX 8.1 compatible
* **OS:** The game may run in different Operating Systems such as Windows, Unix, MacOS.

## Use Cases<a name="use-cases"></a>
### Brief Definition
A use case is a methodology used in system analysis to identify, clarify, and organize system requirements.
The use case is a list of actions or event steps, typically defining the interactions between a role,also know as actor, and a system to achieve a goal.

**Actor-** Actor models a type of role played by an entity, not an individual user of the system, that interacts with the system . Actors are external entities such as people or other systems that interfaces with the developed system.

**Development System-** The software made, it can be an application, a game,etc.

A use case (or set of use cases) has these characteristics:
* Organizes functional requirements.
* Models the goals of system/actor (user) interactions.
* Records paths (called scenarios) from trigger events to goals.
* Is multi-level, so that one use case can use the functionality of another one.

## Domain Model<a name="domain-model"></a>
	TODO: Domain Model
	
## Contributions

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

## Bibliography
Use Case explanations: *http://searchsoftwarequality.techtarget.com/definition/use-case*

