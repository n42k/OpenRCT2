# Report 4: Verification and Validation

## Index
 1. [Introduction](#introduction)
 2. [Test Statistics and analytics](#test_sa)
 3. [Bug identification](#bug_identification)

## Introduction<a name="introduction"></a>

Software testability can be seen as a prediction of the probability that existing faults will be detected during testing. Here, software testability is not regarded as an assessment of the difficulty to select inputs that cover software structure, but as a way to predict whether a program would reveal existing faults during testing. The main reason for seeking testability ratings is to determine early in the software development life cycle how many testing resources will be needed in order to complete the testing process. And typically, the testing process is not completed until some predefined testing stoppage criteria have been satisfied.

####Testability of software components must have in consideration the following:

**Observability:** Software tests examine the outputs produced by the software for particular inputs. This means that software is easier to test if the inputs produce distinct, predictable outputs.

**Controllability:**  The more easily we can provide inputs to the software, the more easily we can test the software. This implies that software is more testable when the tester has the ability to easily control the software in order to provide the test inputs. This controllability applies to the tests as well: tests should be easily specifiable, automated, and reproducible.

**Understandability:** Is the degree to which the component under test is well documented or self-explaining. Therefore, if we pretend to have a flexible and easily understood software, user documentation must be clearly written.

**Isolateability:** Is the degree to which the component under test can be tested in isolation. By breaking down the system into various sections we might be able to spot defects easily in isolation, this isolation can be useful when some particular bugs are really difficult to locate.

**Separation of concerns:** Concerns are different modules of the software. For instance, the logic of a program and his interface are examples of different concerns.
The idea behind it, is to keep the code of each concern separated in order to facilitate the code testing, debugging process and possible changes in the code.

**Heterogeneity:** can be seen as the use of diverse test methods and tools in parallel by taking the maximum advantage of processor/cores.

Nowadays, writing test code and running that same code in parallel with the writting of the software is considered a good habit. This test code, when used correctly, can help the programmer to interpret the program code and its architecture.

Test cases can provide us information about bugs or minor problems within the code, however, if the test result was positive, we may not be able to assume that there aren't any bugs.

Test-driven development (TDD) is one example of a process of software development that is based on code tests. The requirements are transformed into test cases, then the code fragment that has to pass these tests is performed.

There are different phases of software testing, such as:
 * **Unit testing**: The main objective of this phase is to test the smallest amount of software possible. Usually related to software methods;
 * **Integration testing**: In this phase, the various software modules are joined and tested as a whole;
 * **System testing**: Phase where the software, already complete and integrated, is tested. Usually related to the user interface;
 * **Acceptance testing**: It's the phase in which the system is tested for acceptance. The objective is to verify that the system meets the original requirements;
 * **Regression testing**: Phase reponsible for verifying if previously software still performs up to the task and without any problems.

## Test Statistics and analytics<a name="test_sa"></a>

Due to the fact that our project doesn't have tests to support the software code, it isn't possible to obtain test statistics (number of test cases, coverage, etc). An analysis based on static metrics was then made. This can be seen as the examination of a program to verify its quality.

Using the [cloc](http://cloc.sourceforge.net/) tool, it is possible to count the number of lines of code and comments, which allows us to easily establish a ratio between the lines of code and lines of comments.

Output of cloc:
```
486 text files.
458 unique files.                                          
 29 files ignored.

github.com/AlDanial/cloc v 1.70  T=1.34 s (340.2 files/s, 230870.4 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
C                              226          24835          16374         222847
C++                             68           2692           1606          18488
C/C++ Header                   161           2415           3158          17350
Objective C                      1             28             27            222
Markdown                         1             24              0             25
-------------------------------------------------------------------------------
SUM:                           457          29994          21165         258932
-------------------------------------------------------------------------------
```

As we can see, only around 7.6% of the code is comments. This is a low percentage and might indicate a general lack of commenting standards. This could be an issue, as the project might not be documented well enough.

Using the tool [cppcheck](http://cppcheck.sourceforge.net/), we can understand the amount of yet to be fixed errors there are in the code. As the tool describes, it tries to never issue false positives, which means that the true error count is probably slightly higher. Nevertheless, running this tool on OpenRCT2 showed that there probably aren't too many problems with the code. We only ran this on the C++ side of the code as it is quite slow to run, but still allows us to establish a realistic ratio.

Formatted output of cppcheck:
```
[performance][redundantAssignment] Variable 'hash' is reassigned a value before the old one has been used. [src/drawing/engines/opengl/TextureCache.h:38]
[warning][uninitMemberVar] Member variable 'Atlas::_atlasWidth' is not initialized in the constructor. [src/drawing/engines/opengl/TextureCache.h:87]
[warning][uninitMemberVar] Member variable 'Atlas::_atlasHeight' is not initialized in the constructor. [src/drawing/engines/opengl/TextureCache.h:87]
[warning][uninitMemberVar] Member variable 'Atlas::_cols' is not initialized in the constructor. [src/drawing/engines/opengl/TextureCache.h:87]
[warning][uninitMemberVar] Member variable 'Atlas::_rows' is not initialized in the constructor. [src/drawing/engines/opengl/TextureCache.h:87]
[warning][uninitMemberVar] Member variable 'OpenGLDrawingContext::_dpi' is not initialized in the constructor. [src/drawing/engines/opengl/OpenGLDrawingEngine.cpp:503]
[warning][uninitMemberVar] Member variable 'OpenGLDrawingEngine::_bitsDPI' is not initialized in the constructor. [src/drawing/engines/opengl/OpenGLDrawingEngine.cpp:252]
[warning][uninitMemberVar] Member variable 'OpenGLDrawingEngine::GLPalette' is not initialized in the constructor. [src/drawing/engines/opengl/OpenGLDrawingEngine.cpp:252]
[performance][useInitializationList] Variable '_message' is assigned in constructor body. Consider performing initialization in initialization list. [src/core/Exception.hpp:33]
[warning][publicAllocationError] Possible leak in public function. The pointer '_textureCache' is not deallocated before it is allocated. [src/drawing/engines/opengl/OpenGLDrawingEngine.cpp:523]
```

Considering there are 18488 lines of C++ code that were checked, and 10 possible errors, the error rate per line of code is likely extremely low.

Note: you can find how to configure cppcheck for use in OpenRCT2 at the end of the report.

## Contributions
All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

## Bibliography
Marciniak, John  (January 2002). *Encyclopedia of Software Engineering*. 2nd Edition. ISBN 978-0-471-37737-5.

## Notes

### Configuring cppcheck
To configure cppcheck for use with OpenRCT2 on the C++ codebase, create a cppcheck.cmake file in the root directory with the following contents:

```
file(GLOB_RECURSE ALL_SOURCE_FILES *.cpp *.h *.c *.hpp)

add_custom_target(
	cppcheck
	COMMAND /usr/bin/cppcheck
	--enable=information,warning,performance,portability
	--std=c++11
	--template="[{severity}][{id}] {message} {callstack}."
	--quiet
	--suppress=missingIncludeSystem
	--suppress=toomanyconfigs
	--force
	-I /usr/include
	-I /usr/lib
	-I /usr/lib/gcc/*/*/include/
	-I /usr/include/SDL2/
	${ALL_SOURCE_FILES}
)
```

Note that the directories specified by * should be filled in prior to use. There's generally only 1 possible option to use for them, go to /usr/lib/gcc/ for yourself and fill that in manually, depending on your compiler version.

Add ```INCLUDE(cppcheck.cmake)``` to the end of CMakeLists.txt.

Finally, create a build directory and inside this directory run the following commands:
```
cmake ../
make cppcheck
```
