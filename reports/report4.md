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

**Separation of concerns:** Concerns are different modules of the software. The logic of a program and his interface are examples of different concerns.
The basis of the separation of concerns is to keep the code of each concern separated to facilitate the test of the code, the debug and possible changes in the code.

**Heterogeneity:**

Hoje em dia, escrever código de teste e executar esse mesmo código em paralelo com a construção do software é considerado um bom hábito. Este código de teste, quando usado corretamente, pode ajudar a interpretar o código do programa e a respetiva arquitectura.

Um aspeto muito importante, relativo à existência de código de teste, é que estes apenas nos indicam se existem bugs no software, mas caso não sejam indicados bugs não significa que não possam existir.

O processo de desenvolvimento de software Test-driven development (TDD), baseia-se neste facto. Os requisitos são transformados em casos de testes e de seguida é realizado o fragmento de código do programa que tem de passar estes mesmos testes.

Existem diferentes fases de teste do software, nos quais se salientam:
 * Unit testing: O principal objetivo é testar o mais pequeno conjunto de software da aplicação possível. Normalmente relacionado com os métodos do software;
 * Integration testing: Fase na qual os diferentes módulos do software são juntos e testados em conjunto;
 * System testing: Fase de teste de software no qual o software, já completo e integrado é testado. Normalmente relacionado com a interface do software;
 * Acceptance testing: Fase no qual o sistema é testado para aceitação. O objetivo desta fase é verificar a conformidade do sistema com os requisitos iniciais.
 * Regression testing: Fase responsável por verificar se o software que já foi desenvolvido anteriormente ainda continua a executar corretamente e sem quaisquer tipo de erros.
 
## Test Statistics and analytics<a name="test_sa"></a>

Devido ao facto do nosso projeto não ter testes ao código do software, não foi possível obter as suas estatísticas (número de casos de teste, cobertura, etc). Foi então realizada uma análise à base de métricas estáticas.

A análise à base de métricas estáticas pode ser visto como a examinação e análise de um programa para verificação da sua qualidade.


## Contributions
All 4 group members have contributed evenly to the report:

* João 'TUTAMKHAMON' Ferreira.
* Jorge 'Jorge2210' Ferreira.
* Pedro 'n42k' Amaro.
* Pedro 'Oshnira' Lima.

## Bibliography
Marciniak, John  (January 2002). *Encyclopedia of Software Engineering*. 2nd Edition. ISBN 978-0-471-37737-5.

