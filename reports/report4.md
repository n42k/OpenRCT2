# Report 4: Verification and Validation

## Index
 1. [Introduction](#introduction)
 2. [Test Statistics and analytics](#test_sa)
 3. [Bug identification](#bug_identification)

## Introduction<a name="introduction"></a>

Software testability can be seen as a prediction of the probability that existing faults will be detected during testing. Here, software testability is not regarded as an assessment of the difficulty to select inputs that cover software structure, but as a way to predict whether a program would reveal existing faults during testing. The main reason for seeking testability ratings is to determine early in the software development life cycle how many testing resources will be needed in order to complete the testing process. And typically, the testing process is not completed until some predefined testing stoppage criteria have been satisfied.

Testability is regarded as a measure of the difficulty to establish a test criteria and the performance of tests to determine whether those criteria have been met and it's usually determined by two main problems: how to define the test cases and what behavior we might expect.

**Observability:** Software tests examine the outputs produced by the software for particular inputs. This means that software is easier to test if the inputs produce distinct, predictable outputs. 

**Controllability:**  The more easily we can provide inputs to the software, the more easily we can test the software. This implies that software is more testable when the tester has the ability to easily control the software in order to provide the test inputs. This controllability applies to the tests as well: tests should be easily specifiable, automated, and reproducible.


## Bibliography
Marciniak, John  (January 2002). *Encyclopedia of Software Engineering*. 2nd Edition. ISBN 978-0-471-37737-5.

