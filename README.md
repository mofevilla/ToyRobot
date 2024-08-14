
ToyRobot Project Overview

Description and requirements:

    The application is a simulation of a toy robot moving on a square table top, of dimensions 5 units x 5 units. There are no other obstructions on the table surface. The robot is free to roam around the surface of the table, but must be prevented from falling to destruction. Any movement that would result in the robot falling from the table must be prevented, however further valid movement commands must still be allowed. Create a console application that can read in commands of the following form -
    PLACE X,Y,F
    MOVE
    LEFT
    RIGHT
    REPORT
    
    PLACE will put the toy robot on the table in position X,Y and facing NORTH, SOUTH, EAST or WEST. The origin (0,0) can be considered to be the SOUTH WEST most corner. It is required that the first command to the robot is a PLACE command, after that, any sequence of commands may be issued, in any order, including another PLACE command. The application should discard all commands in the sequence until a valid PLACE command has been executed. 
    MOVE will move the toy robot one unit forward in the direction it is currently facing.  
    LEFT and RIGHT will rotate the robot 90 degrees in the specified direction without changing the position of the robot. 
    REPORT will announce the X,Y and F of the robot. This can be in any form, but standard output is sufficient. 
    
    A robot that is not on the table can choose to ignore the MOVE, LEFT, RIGHT and REPORT commands. Input can be from a file, or from standard input, as the developer chooses. Provide test data to exercise the application. It is not required to provide any graphical output showing the movement of the toy robot. The application should handle error states appropriately and be robust to user input.


Constraints:
    The toy robot must not fall off the table during movement. This also includes the initial placement of the toy robot. Any move that would cause the robot to fall must be ignored.


Setup:
    
    1. Open the solution file (ToyRobot.sln) by double-clicking it or by launching it in Visual Studio.

Building the project:

    1. In Visual Studio, select target "Release" and architecture "x86"
    2. In Menu > select Build > Rebuild Solution
Running ToyRobot:

    A. In Visual Studio
        1. Click Local Windows Debugger then type the commands on the command line
    B. Run executable
        1. Run the executable file (.exe) in <solution folder>\Release\ToyRobot.exe by double clicking on it and typing the commands  
    C. Via command line
        1. cd to <solution folder>\Release
        2. Type ToyRobot.exe then press enter
            - Type the commands on the command line
        3. Or Type ToyRobot.exe <absolute path to test case text file>

Running ToyRobotTest:

    1. In Menu > select Test > Run > All Tests


Files:

ToyRobot

main.cpp
- contains the main() function
- Passes the command to the Controller to parse

controller.h, contoller.cpp
- handles the parsing and validating of commands
	
toyrobot.h, toyrobot.cpp

- contains the constants for table size, enum for direction 
- contains the logic of each action and keeps the Toy Robot in bounds
	
toyrobot_input_sample.txt

- sample input file that can be used as parameter when running: ToyRobot.exe <absolute path to toyrobot_input_sample.txt>


ToyRobotTest

toyrobottest.cpp

- contains the unit tests for ToyRobot class
- Current tests:
	
        ToyRobot_Constructor
		ToyRobot_Place_0_0_N
		ToyRobot_Place_2_3_W
		ToyRobot_Place_OutofBounds
		ToyRobot_Move_X
		ToyRobot_Move_Y
		ToyRobot_Move_X_OutofBounds
		ToyRobot_Move_Y_OutofBounds
		ToyRobot_Move_Unplaced
		ToyRobot_Left
		ToyRobot_Right
		ToyRobot_Left_Unplaced
		ToyRobot_Right_Unplaced
