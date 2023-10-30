
# Documentation Rtype



## Introduction



The Rtype project is a multimedia application that combines a custom Game Engine, Entity-Component System (ECS), web interface, GUI, and client-server architecture. This document aims to provide an overview of the project and guide developers, designers and users through its different components.





## How to launch (hard way)


### Linux compilation:

First step , creat a build folder for compiling, execut this command in the root of the project:



	.`cmake -B build`



(It might take a while)




Last step, compile the project with this command:



	.`cmake --build build`


### Windows compilation:

First step , creat a build folder for compiling, execut this command in the root of the project:



	`cmake . -B Build -G "MinGW Makefiles"`



(It might take a while)




Last step, compile the project with this command:



	`cmake --build Build`


-------------------

## How to launch (easy way)

### Linux compilation:

Execute the "build_project.sh" file with the command:

	`./build_project.sh`


### Windows compilation:

Execute the "build_project.bat" file with the command:

	`./build_project.bat`

## Finaly

After compilation you will have 2 executables, one for the server (`server` or `server.exe` on windows) and one for the client (`client` or `client.exe` on windows).

Execute this file for launch the programe (server part and client part).

## Dependencies

Your project use the Network library [**ASIO**](https://think-async.com/Asio/Documentation.html) and the graphical library [**SFML**](https://www.sfml-dev.org/documentation/2.6.0/)

## Authors

We are a team of 5 people, **Allevard Matteo** and **Killian Lachaud** for the network server side and documentation, **Ryan Thouvenel** and **Valentin Grisel** for the ECS and Game Engine server side, **Hugo Des Mares De Trébons** for all the Client side.

[Developer Documentation](./docs/general_doc.md)


