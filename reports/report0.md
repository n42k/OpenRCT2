# Software Processes in OpenRCT2

## Index
1. [Brief description](#brief)
2. [Development Process](#development_process)
1. [Initial development](#initial_development)
2. [Current development](#current_development)
3. [Opinions, critics and alternatives](#opinions)

## Brief description <a name="brief"></a>
OpenRCT2 is an open source re-implementation of the RCT2 (RollerCoaster Tycoon 2) game. RCT2 is an amusement park construction and management simulation computer game.
It was started in 2014 by a single person, Ted "IntelOrca" John, with the intent of modernizing upon the original game as well as porting it to other operating systems.
At the time of writing, it has 142 contributors with approximately 10,939 commits.
The core language is C and it was painfully reverse engineered from the original game executable.

![alt tag](https://github.com/n42k/OpenRCT2/blob/783b5911df1de6a34f0d7713f8033c74a9e8b654/reports/Images/Languages%20Graphical1.png)
![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/1.png)
**Fig1-** Graphic representing lines of code per language used in project. 

## Development Process <a name="development_process"></a>
### Initial development <a name="initial_development"></a>
Having its roots in the hands of a single person, it probably didn't start with a specific development process. However, it was reverse engineered from the original game executable in an interesting way: a single function was re-implemented from the executable at a time and, by use of regression testing against the original game, tested to make sure it does what it's supposed to do.

### Current development <a name="current_development"></a>
At the current time, there are many collaborators for the project's evolution, even though the founder continues to be the largest contributor. The contributors join together in a chatroom (gitter.im) to exchange ideas about the project itself and the various improvements that can be done to it.
Periodically, new stable releases are launched, with several updates and bugfixes.

The project uses the gitflow workflow. It's centered around the use of a vast set of new commands, each executing a group of tasks in a predefined order. This does not replace git, it's only a set of scripts that use the standard git commands in a smart way. It's possible to use the standard git commands, in the correct order and with the right arguments, to follow a specific workflow. However, using gitflow it is not necessary to memorize these.

## Opinions, critics and alternatives <a name="opinions"></a>
Por, inicialmente, o projeto ser de apenas uma pessoa, não existia necessidade de comentar o código em grande quantidade, sendo que atualmente, com o aumento dos colaboradores, este aspeto é uma desvantagem. Apenas 7% do código é comentado. Um alto número de comentários pode ser indicador de um código bem estruturado e organizado e, por sua vez, melhora a interpretação de toda a equipa de desenvolvimento. 

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
	Whether the project was started with the idea of making it by himself.
	Why the project was started.
	Is there any development process?
