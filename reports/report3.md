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

In simple terms, each of these views is concerned about the following:
* The Logical View: this view is concerned with the functional requirements of the software system, and abstracts them into software packages/classes. It can be represented by a package diagram, for example.
* The Process View: this view handles some non-functional requirements, such as performance or availability, and the data flow of the program, so that we can see what could be run in parallel, for example. This view can be represented by an Activity Diagram, which shows the flow from one activity to another.
* The Physical View: this view takes care of mainly non-functional requirements, such as scalability, performance, throughput and availability. It maps a piece of software to the hardware that will run it, and the flow of data that the hardware/software will pass between each other. It can also be called the Deployment View, which we did on this report. It can be represented by a deployment diagram.
* The Development View: this view divides the program in small subsystems that can be programmed independently by a small group of developers. This will later be used to assign tasks to teams and estimate costs, for example. It may be represented by a component diagram.
* The Use Cases View: a redundant view, considering we already have the other 4 ones, but it will serve as a simple diagram that can be followed to create a prototype of the software package.

In OpenRCT2, we do not believe that any specific software architecture was followed. As we can see in the Logical View, there's lots of dependencies between packages, which might have been able to be heavily simplified. There can also be an implicit layered architecture, with the lower level code at the bottom, dealing with graphics and sound and other low level tasks, but that is not clearly specified, as every 'package' is at the same level.

## Logical View<a name="logical_view"></a>
In the context of our game, since it uses the C programming language, we have considered a package a folder which contains C source code files.
Thus, we consider that there is a link between one package and another if in first package there are files that include files from the second package.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/logical_view.png)
**Fig1** - Logical View of OpenRTC2

Due to the huge complexity of the OpenRCT2, there’s a big interconnection between its packages. The fact that the whole game has been reverse engineered from the original executable based on the assembly, makes it so that most part of the packages have a huge dependency on a great number of other packages.

## Development View<a name="development_view"></a>
The development view for OpenRCT2 is quite simple, as it only depends on a few libraries for running. The Twitch integration was also added in this diagram, since it was fitting (and this diagram only).

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/ComponentDiagram.png)

**Fig2** - Development View - Component Diagram - OpenRCT2

## Deployment View<a name="deployment_view"></a>
For OpenRTC2 the deployment view is very simple as it only needs a working computer for it to run.
![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/Deployment%20View.png)
**Fig3** - Deployment view - OpenRTC2

## Process View<a name="process_view"></a>
In OpenRCT2, the process view model focuses on in-game interactions, interfaces and it can be easily understood by analysing the diagram due to the fact that recursion and activities flow is quite similiar to other games.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/ProcessViewModel.png)
**Fig4** - Process View model.

## Contributions
All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

## Bibliography

McConnell, Steve (June 2004). "Design in Construction". Code Complete (2nd ed.). Microsoft Press. p. 29. ISBN 978-0-7356-1967-8. "Chapter 3: Measure Twice, Cut Once: Upstream Prerequisites"

Philippe Kruchten (November 1995). "Architectural Blueprints – the 4+1 View Model of Software Architecture". IEEE Software. 12 (6). pp. 42–50
