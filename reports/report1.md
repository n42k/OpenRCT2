# Report 1: Software Processes in OpenRCT2

## Index
1. [Brief description](#brief)
2. [Development Process](#development_process)
	1. [Initial development](#initial_development)
	2. [Current development](#current_development)
3. [Opinions, critics and alternatives](#opinions)

## Brief description <a name="brief"></a>
RollerCoaster Tycoon 2 (RCT2) was a construction and management simulation computer game lauched in 2002 where you played as an amusement park manager. Over the years the official game support finally got to an end which prompted the arise of a fan-made project, led by Ted 'IntelOrca' John, with the intent of reverse engineering the original RCT2 executable. 
The OpenRCT2 project was then launched in April 2014 with the set goals of:
* Porting the game into platform independent C source code, making the game available to more platforms;
* Fix [bugs][1] the lasted over the years on the no longer supported game;
* Add [translations][2] to the game's user interface;
* Add support for higher resolution to accommodate for nowadays technology;
* Add online multiplayer functionality;
* And other minor [features][3] like simulation speed increase and twitch integration...

[1]: https://github.com/OpenRCT2/OpenRCT2/wiki/Found-bugs-and-limitations-in-RCT2
[2]: https://github.com/OpenRCT2/OpenRCT2/wiki/Language-support
[3]: http://openrct2.org/features

At the time of writing, the project is hosted on GitHub under GPLv3 license and requires the original game files to run (mainly resources and content). It's core language is C, with some bits of C++ along the way, and it has accumulated 142 contributors and approximately 11,000 commits along the years.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/cd5004fa67ed5e11e02761288cea1c82826622c1/reports/Images/Languages%20Graphical1.png)
**Fig1-** Lines of code per language over time graph.
![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/1.png)
**Fig2-** Lines of code per language graph.

## Development Process <a name="development_process"></a>
### Initial development <a name="initial_development"></a>
Having its roots in the hands of a single person, it probably didn't start with a specific development process. However, it was reverse engineered *(1)* from the original game executable in an interesting way: a single function was re-implemented from the executable at a time and, by use of regression testing against the original game, tested to make sure it does what it's supposed to do.


*(1)*  It can also be seen as "going backwards through the development cycle". The output of the implementation phase (in source code form) is reverse-engineered back to the analysis phase, in an inversion of the traditional waterfall model.

### Current development <a name="current_development"></a>
At the current time, there are many collaborators for the project's evolution, even though the founder continues to be the largest contributor. The contributors join together in a chatroom (gitter.im) to exchange ideas about the project itself and the various improvements that can be done to it.
Periodically, new stable releases are launched, with several updates and bugfixes.

The project uses the gitflow workflow. It's centered around the use of a vast set of new commands, each executing a group of tasks in a predefined order. This does not replace git, it's only a set of scripts that use the standard git commands in a smart way. It's possible to use the standard git commands, in the correct order and with the right arguments, to follow a specific workflow. However, using gitflow it is not necessary to memorize these.

## Opinions, critics and alternatives <a name="opinions"></a>
Since initially the project was run by a single person there was no need to mass comment the code, making it a disadvantage now that the amount of collaborators has increased. Only about 7% of lines are comments. A higher comment count could be an indicator of well structured and organized code, and in turn, helps everyone involved to better understand the code.

According to the statistics, over the past twelve months, 130 developers contributed new code to OpenRCT2. So, that means the project is getting more and more interesting for open source community. Although, there isn't any project planning yet and makes it harder for new contributors since they don't know where exactly they should start by.
Also, having a decent planning leads to a significant increase of efficiency of everyone working on the project. But why? Well, highlighting the most important, we got the following:
* Coordination between contributors;
* Good environment;
* Work getting tracked over time (such as progress, time cost, etc);
* Guide the work in order to know exactly what to do next.
By now it should be clear why we must follow some planning.

## Contributions
All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

### TODO:
	Is there any development process?
