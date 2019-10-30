# Arma3EMPmultiplayer

A modified version of the Arma 3 EMP script by Aliascartoons on [Armaholic](http://www.armaholic.com/page.php?id=34293). Edited by Kasteelharry for useage in multiplayer and to be used in combination with the TFAR jamming script by Rebel12340 on [Armaholic](http://www.armaholic.com/page.php?id=32660).

## Installation guide

1. Clone or download the repository and place all the files and folders in your mission folder.
2. Copy contents of any already existing files over to the correct files.
3. In the editor give the object that serves as the EMP source the variable name ***EMP***.
   - If the object already has a variable name, change it in the initServer.sqf or set the variable "EMP" as shown in usage.
4. Set the range and strength of the EMP and Jammers in the initServer.sqf file.

## Usage

- In your mission place down the object that will function as your EMP/jammer and give it a variable name.
- Run the following line of code global:

```sqf
[EMP,EMP_Range,true,true] execvm "AL_emp\emp_starter.sqf";
```

- where EMP is the variable name you have given to the object in the editor and range is the EMP_Range of the emp blast.
  - Changeable in initServer.sqf
    - Or with:

```sqf
//Sets the variable from where to run the EMP
missionNamespace setVariable ["EMP", _EMPvariables, true];
//Sets the range of it
missionNamespace setVariable ["EMP_Range", _EMP_Range, true];
```

- To stop the TFAR Jamming script delete the object with the EMP variable name.

## Upcoming features

1) A way to automatically stop the jamming/whitelist players, after, for example, finding intel, walking out the range and back in or rearming at an arsenal.

## Known Bugs

- Toolkits are not removed from the players inventories.
