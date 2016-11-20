# Report 3: Software Design

## Index
 1. [Introduction](#introduction)
 2. [Logical View](#logical_view)
 3. [Development View](#development_view)
 4. [Deployment View](#deployment_view)
 4. [Process View](#process_view)


## Introduction<a name="introduction"></a>
Software architecture is a metaphor for real world building architecture. Just like buildings are designed by an architect to prevent costly modifications after the building is built, software can also be designed this way. Doing so, whether more formally (for business projects) or more informally (for hobby projects), tends to reduce implementation issues that may arise during that phase, and as we've seen in the report about requirements, that will translate to higher costs, as more work is done in the latter phases of the project that could be entirely avoided if planned for.

The 4+1 Architectural View Model, as designed by Philippe Kruchten, is a methodology to draw diagrams to represent a software system. It tries to separate the concerns of the various stakeholders by providing separate diagrams instead of a single one, as was often the case when the author described this method. As the name implies, it consists of 5 diagrams: the logical view, the process view, the physical view, the development view and a view that joins the previous 4, which can be called a use cases view.

*TODO: describe each view in turn.*

In OpenRCT2, we do not believe that any specific software architecture was followed. As we can see in the Logical View, there's lots of dependencies between packages, which might have been able to be heavily simplified. There can also be an implicit layered architecture, with the lower level code at the bottom, dealing with graphics and sound and other low level tasks, but that is not clearly specified, as every 'package' is at the same level.

## Logical View<a name="logical_view"></a>
In the context of our game, we consider packages into every division by code files folders.
According to the above mentioned, we consider that there is a link between one package and another if in the first package there are files that include files from the second package.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/logical_view.png)
**Fig1** - Logical View of OpenRTC2

Due to the huge complexity of the OpenRCT2, there’s a big interconnection between its packages. The fact that the whole game has been reverse engineered from the original executable based on the assembly, makes it so that most part of the packages have a huge dependency on a great number of other packages.
## Development View<a name="development_view"></a>
![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/ComponentDiagram.png)

**Fig2** - Development View - Component Diagram - OpenRCT2

## Deployment View<a name="deployment_view"></a>
A deployment view model allows us to understand the hardware and sotware needs of a program.
For OpenRTC2 the deployement model is very simple as it only needs a working computer for it to run. The deployment diagram for the game looks like this:
![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/Deployment%20View.png)
**Fig3** - Deployment view - OpenRTC2

## Process View<a name="process_view"></a>
The Process view shows tasks and processes that the system has, interfaces to the outside world and/or between components within the system and focuses on the runtime behavior of the system. This model is represented by Activity diagram.

An **Activity diagram** is like a flowchart, as it shows the flow from one activity to another.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/ProcessViewModel.png)
**Fig4** - Process View model.

For OpenRCT2, the process view model focuses on In-Game interactions, interfaces and it can be easily understood by analysing the diagram due to the fact that recursion and activities flow is quite similiar to other games.

## Contributions

All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.
