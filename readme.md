# Robot Abstraction Coursework
![Build](https://img.shields.io/badge/Test-Pass-success) ![Language](https://img.shields.io/badge/Language-C-informational)					![Course](https://img.shields.io/badge/Course-COMP0002-important) ![Author](https://img.shields.io/badge/Author-Jianheng.H-important) ![Date](https://img.shields.io/badge/Date-09%2F11%2F2021-red)  



## Introduction 
The purpose of this program is to direct the robot to the marker by avoiding obstacles on a 10 by 10 grid. The program generates the grid as well as the objects, namely the robot as a green triangle, the marker as a grey square and the obstacles (Blocks) as red squares on the grid. 

![https://imgur.com/8kkTJZy.png](https://imgur.com/8kkTJZy.png)
## How it works ?
In this program, the robot can move forward, turn left and turn right, but is not able to move onto the obstacles (Blocks). It can move freely onto white spaces and the marker.

There are 2 modes to finding the marker. In the case of "random" mode, the robot randomly moves forward, turn left and turn right. The actions: forward, left and right are weighted differently, such that the robot is more likely to move forward than turning left or right, where turning left is just as likely as turning right.

In the case of "algorithmic" mode, the robot goes through all the squares on the grid at least once, which guarantee the robot finding the marker.

## Requirements
Compiler: `gcc`

Files:
`abstraction.c`
`graphics.c`
`graphics.h`
`drawapp-2.0.jar`

Link to drawapp: `https://moodle.ucl.ac.uk/mod/resource/view.php?id=3199724`

## Usage
Type the following into the Terminal:

Compile: `gcc abstraction.c graphics.c`

Format:  `./a.out (initial_x_pos) (initial_y_pos) (direction) (mode) | java -jar drawapp-2.0.jar`

Constraints:  
`1.Initial x and y positions of the robot cannot be set on top of an existing marker or blocks and both must be in the range of 0-9.`
`2. 4 directions: {north, east, south, west}`
`3. 2 modes: {random, algorithmic}`

Examples:
Run(random Mode) - Starting position (0,1); Direction - South: 
`./a.out 0 1 south random | java -jar drawapp-2.0.jar`

Run(algorithmic Mode) - Starting position (1,9); Direction - North: 
`./a.out 1 9 north algorithmic | java -jar drawapp-2.0.jar`

**UCL - Department of Computer Science**
