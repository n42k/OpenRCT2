# Report 3: Software Design
 
## Index
 1. [Introduction](#introduction)
 2. [Logical View](#logical_view)
 3. [Development View](#development_view)
 4. [Deployment View](#deployment_view)
 4. [Process View](#process_view)

 
## Introduction<a name="introduction"></a>
 
## Logical View<a name="logical_view"></a>
In the context of our game, we consider packages into every division by code files folders.
According to the above mentioned, we consider that exists a link between one package to another if in the first package there are files that include files from the second package.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/logical_view.png)
**Fig1** - Logical View of OpenRTC2

Due to the huge complexity of the OpenRCT2, there’s an interconnection between its packages. The fact that the whole game has been reverse engineered from the original executable based on the assembly makes that the most part of the packages have a huge dependency of great number of other packages.
## Development View<a name="development_view"></a>
   
## Deployment View<a name="deployment_view"></a>
 
## Process View<a name="process_view"></a>
The Process view shows tasks and processes that the system has, interfaces to the outside world and/or between components within the system and focuses on the runtime behavior of the system. This model is represented by Activity diagram.

An **Activity diagram** is kinda of a flowchart, as long as it shows the flow from one activity to another.

![alt tag](https://raw.githubusercontent.com/n42k/OpenRCT2/develop/reports/Images/ProcessViewModel.png)
**Fig4** - Process View model.
