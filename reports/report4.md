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
 * **Unit testing**: O principal objetivo é testar o mais pequeno conjunto de software da aplicação possível. Normalmente relacionado com os métodos do software;
 * **Integration testing**: Fase na qual os diferentes módulos do software são juntos e testados em conjunto;
 * **System testing**: Fase de teste de software no qual o software, já completo e integrado é testado. Normalmente relacionado com a interface do software;
 * **Acceptance testing**: Fase no qual o sistema é testado para aceitação. O objetivo desta fase é verificar a conformidade do sistema com os requisitos iniciais.
 * **Regression testing**: Fase responsável por verificar se o software que já foi desenvolvido anteriormente ainda continua a executar corretamente e sem quaisquer tipo de erros.
 
## Test Statistics and analytics<a name="test_sa"></a>

Duo to the fact that our project doesn't have tests to support the software code, it isn't possible to obtain statistics (number of test cases, coverage, etc). An analysis based on static metrics was then made.

The analysis based on static metrics can be seen as the examination of a program to verify its quality.

## Contributions
All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

## Bibliography
Marciniak, John  (January 2002). *Encyclopedia of Software Engineering*. 2nd Edition. ISBN 978-0-471-37737-5.

