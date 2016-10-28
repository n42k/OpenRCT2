# Report 2: Requirements Elicitation

## Index
1. [Requirements](#requirements)
	1. [Introduction](#introduction)
	2. [Purpose/Scope](#purpose/scope)
	3. [Description](#description)
2. [Specific Requirements and Features](#specific-requirements)
3. [Use Cases](#use-cases)
4. [Domain Model](#domain-model)

## Requirements <a name="requirements"></a>
### Introduction <a name="introduction"></a>
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
 * ...

### Non-Functional requirements
#### User requirements
* O jogo deve estar optimizado e, por consequência, possuir um número considerável de frames per second;

#### System requirements
* Processor (CPU): Pentium III
* System memory (RAM): 64 MB
* Hard disk drive(HDD): 800MB
* Video card (GPU): 8 MB of VRAM, DirectX 8.1 compatible
* The game may run in different Operating Systems such as Windows, Unix, MacOS.

## Use Cases<a name="use-cases"></a>
	TODO: Use Cases **including diagrams**
## Domain Model<a name="domain-model"></a>
	TODO: Domain Model
