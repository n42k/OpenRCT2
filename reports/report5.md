# Report 5: Software Maintenance/Evolution

## Index
1. [Software Maintainability](#software_maintainability)
2. [Evolution Process](#evolution_process)
3. [Pull Request](#pull_request)

## Software Maintainability<a name="software_maintainability"></a>
[![BCH compliance](https://bettercodehub.com/edge/badge/n42k/OpenRCT2)](https://bettercodehub.com)

Discuss Software Maintanability using the SIG metrics here.

## Evolution Process<a name="evolution_process"></a>
The feature that was decided to implement was identified by the OpenRCT2 collaborators themselves, and marked as a possible improvement in the program for those who want to implement it.
The feature consistes in prevent the auto-save if the game is in pause and nothing has been done. This way, we prevent the creation of multiple slots with the same save.
For example, if in the game options is selected to save the game every 5 minutes, and at the minute 1, the game is paused (where nothing is being changed), the game is only saved automatically after 4th minute after resuming. In this way, the pause is not counted as time for the save and the time passed before the pause is counted to keep the logic of saving the game every 5 minutes.

**Briefly** describe how the feature you decided to evolve was identified, why did you decide to evolve that particular feature and how the parts in the source code that needed to be modified were located.

## Pull Request<a name="pull_request"></a>
Link the PR here.
