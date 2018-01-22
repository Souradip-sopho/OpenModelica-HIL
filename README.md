# OpenModelica-HIL-Simulation
Free library for Hardware-in-Loop simulation with Arduino using Modelica and Modelica_DeviceDrivers models in Linux. 

## Library description
The `OpenModelica-HIL-Simulation` library is an open source Modelica package for Hardware-in-Loop simulations  involving Arduino platforms using Interprocess Communication.

Main features:
  * Support for Linux.
  * (Soft) real-time synchronization of a simulation.
  
Please note that the library is known to work with
* OpenModelica (partial support starting with OpenModelica v1.11.0, e.g.serial port).

## Prerequisites
  * `OpenModelica` (>= v1.11.0) (https://www.openmodelica.org/download/download-linux)
  * `Modelica_DeviceDrivers` (v1.5.1) (https://github.com/modelica/Modelica_DeviceDrivers/releases/tag/v1.5.1)
  * `Servomechanisms`(https://github.com/afrhu/Servomechanisms.git)


* Install and Run:
Launch OMEdit and load the package `OpenModelica-HIL-Simulation` and `InterProcessCommunication'.Also, load the `Servomechanisms` package present in the directory.Load the Arduino platform with the `cotroller.ino` code.Create any model using the package and simulate.

## Running Test Simulation
  Test the package using `HIL_Arduino.mo` test provided.
  * Load the Arduino platform with the `controller.ino` code.
  * Compile the SerialSHM.c file using the following command
  ```
  $ gcc Serial_SHM.c -o Serial_SHM 
  ```
  * Execute the SerialSHM file using the following command
  ```
  $ sudo ./Serial_SHM
  ```
  * Load the `HIL_Arduino.mo` test model present in package.
  * Simulate the model.If no error occurs,the package is good to go.
  
For further information:  Visit https://build.openmodelica.org/Documentation/Modelica.html,https://build.openmodelica.org/Documentation/Servomechanisms.html

## Development and contribution
Main developers:
* [Souradip Pal](https://github.com/Souradip-sopho), contribution to the Linux specific code

Contributions in shape of [Pull Requests] are always welcome.

The following people have directly contributed to the implementation of the library (many more have contributed by providing feedback and suggestions):
* Manas Ranjan Das (project mentor), contribution in bug fixes,error removal etc.
