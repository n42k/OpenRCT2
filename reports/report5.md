# Report 5: Software Maintenance/Evolution

## Index
1. [Software Maintainability](#software_maintainability)
2. [Evolution Process](#evolution_process)
3. [Pull Request](#pull_request)

## Software Maintainability<a name="software_maintainability"></a>

The ease or difficulty with which a software system can be modified is known as maintainability. The maintainability of a software system is determined by properties of its source code.

[![BCH compliance](https://bettercodehub.com/edge/badge/n42k/OpenRCT2)](https://bettercodehub.com)

As can be seen in the [bettercodehub](https://bettercodehub.com) website, OpenRCT2 complies with 3 of their metrics. Although that doesn't seem too good, it does line up with what the OpenRCT2 developers have been saying: it is in need of a major refactor.

Amongst the 7 metrics it doesn't comply with, we can highlight a few of the most important ones:

**Writing Short Units of Code**: SIG recommends writing units with at most 15 lines of code and, if this limit is surpassed, to decrease the size of units by dividing them into more units. Over 50% of OpenRCT2's code is composed of units with more than 30 lines of code, which shows that this metric was not obeyed.

**Writing Simple Units of Code**: by reducing the number of branching statements in our code, we can reduce its inherent complexity. If a unit has too many branching points, we can improve it the same way we solved the problem above: taking a few points to another unit. In OpenRCT2, around 50% of units have over 10 branching points. The worst offender in its codebase has 114 branching points (the surface_paint function in paint/map_element/surface.c). By refactoring the worst issues into smaller units, we can greatly improve the maintainability of the codebase.

**Simple Units of Code** makes it easier to modify and test.

**Code Written Once** avoids code and error multiplication.

**Separate Concerns in Modules** identify and extract responsibilities of large modules to separate modules and hide implementation details behind interfaces.

**Architecture Components Balanced** Balancing the number and relative size of components makes it easier to locate code.

**Couple Architecture Components Loosely** components makes it easier to maintain components in isolation.

**Automate Tests**: Automating tests for the codebase makes development more predictable and less risky. We must add tests for existing code every time we change it. According to SIG, in average, we must have at least 50% of the total lines of production code. In OpenRCT2, there are 250.498 of code lines, with only 2,338 of lines of test that makes only 1% test code percentage.

**Write Clean Code**: Clean code is more maintainable.

**Codebase Small** maintainability slightly increases.

Discuss Software Maintanability using the SIG metrics here.

## Evolution Process<a name="evolution_process"></a>
The feature that was decided to implement was identified by the OpenRCT2 collaborators themselves, and marked as a possible improvement in the program for those who want to implement it.
The feature consistes in prevent the auto-save if the game is in pause and nothing has been done. This way, we prevent the creation of multiple slots with the same save.

For example, if in the game options is selected to save the game every 5 minutes, and at the minute 1, the game is paused (where nothing is being changed), the game is only saved automatically after 4th minute after resuming. In this way, the pause is not counted as time for the save and the time passed before the pause is counted to keep the logic of saving the game every 5 minutes.

The choice of this feature was made based on the time we had and how challenging it would be for us to implement it.  

**Briefly** describe how the feature you decided to evolve was identified, why did you decide to evolve that particular feature and how the parts in the source code that needed to be modified were located.

## Pull Request<a name="pull_request"></a>
The pull request can be found in the following link: https://github.com/OpenRCT2/OpenRCT2/pull/4892 .

## Contributions
All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.
