# Report 5: Software Maintenance/Evolution

## Index
1. [Software Maintainability](#software_maintainability)
2. [Evolution Process](#evolution_process)
3. [Pull Request](#pull_request)

## Software Maintainability<a name="software_maintainability"></a>

The ease or difficulty with which a software system can be modified is known as maintainability and is determined from the properties of its source code.

[![BCH compliance](https://bettercodehub.com/edge/badge/n42k/OpenRCT2)](https://bettercodehub.com)

As can be seen in the [bettercodehub](https://bettercodehub.com) website, OpenRCT2 complies with 3 of their metrics. Although that doesn't seem too good, it does line up with what the OpenRCT2 developers have been saying: it is in need of a major refactor.

The 7 metrics which it doesn't obey are the following:

**Writing Short Units of Code**: SIG recommends writing units with at most 15 lines of code and, if this limit is surpassed, to decrease the size of units by dividing them into more units. Over 50% of OpenRCT2's code is composed of units with more than 30 lines of code, which shows that this metric was not obeyed.

**Writing Simple Units of Code**: by reducing the number of branching statements in our code, we can reduce its inherent complexity. If a unit has too many branching points, we can improve it the same way we solved the problem above: taking a few branches to another unit. In OpenRCT2, around 50% of units have over 10 branching points. The worst offender in its codebase has 114 branching points (the surface_paint function in paint/map_element/surface.c). By refactoring the worst issues into smaller units, we can greatly improve the maintainability of the codebase.

**Write Code Once**: writing code once is relatively important for maintenance: if a bug appears, and the code is properly organized, there is only a need to fix it in one place. Thus, we must avoid duplication of code at all costs. According to SIG, we can reduce duplication by extracting shared code, either to a new unit or to a superclass. In OpenRCT2, there are a lot of modules that not obey this metric. This is mostly due to the fact that data is stored in the source code and many values (such as 0) are repeated hundreds of times in arrays.

**Keep Unit Interfaces Small**: keeping the number of parameters low makes units easier to understand and reuse. According to SIG the maximum number of parameters per unit must be at most 4. Clearly, OpenRCT2 doesn't follow this, as there are a large number of units with more than 6 parameters.

**Separate Concerns in Modules**: by separating concerns in modules it makes it easier to understand the code, minimizing the cost associated with changing the codebase. If we want to follow this advisory, we must, firstly, identify, and then extract responsibilities of large modules to other smaller modules and hide implementation details behind interfaces.

**Automate Tests**: having automated tests in a codebase allows developers to know if any change they made breaks their software in unexpected ways. Having a good amount of automated tests and adding new tests every time you change the code will improve this metric. According to SIG, we should have 50% of the code in OpenRCT2 be automated tests. As only 1% of the code in this project is classified as tests, this metric fails.

**Keep Your Codebase Small**: it's well known that changing small amounts of code is easier than changing big chunks of code. By refactoring code to have the same functionality and a simpler implementation, or simply using available libraries or frameworks is a good way of keeping codebase size low. The bettercodehub website suggests always keeping a software system's volume below 20 man-years. OpenRCT2's volume is 21.8 man-years, which isn't too bad, considering it is almost fully implemented and the developers are aware of its issues.

## Evolution Process<a name="evolution_process"></a>
The feature that we decided to implement was identified by the OpenRCT2 collaborators themselves, and marked as a possible improvement in the program for those who want to implement it.
The feature consists in prevent the auto-save feature if the game is paused and nothing has been done ingame. This way, we prevent the creation of multiple, equal, saves.

For example, if we selected in the game options to save the game every 5 minutes, and at the 1st minute, the game is paused, the game is only saved automatically after 4 minutes have passed since we resumed the game. This way, the pausing is not counted as time for the save and the time passed before the pause is counted to keep the logic of saving the game every 5 minutes.

The choice of this feature was made based on the time we had and how challenging it would be for us to implement it.

## Pull Request<a name="pull_request"></a>
The pull request can be found in the following link: https://github.com/OpenRCT2/OpenRCT2/pull/4892 .

## Contributions
All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

## Bibliography
[1] “Better Code Hub” bettercodehub.com. Accessed at 5 Dec. 2016.
