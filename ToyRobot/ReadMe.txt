========================================================================
    APPLICATION : ToyRobot Project Overview
========================================================================
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

controller.h
contoller.cpp
	- handles the parsing and validating of commands
	
toyrobot.h
toyrobot.cpp
	- contains the constants for table size, enum for direction 
	- contains the logic of each action and keeps the Toy Robot in bounds
	
toyrobot_input_sample.txt
	- sample input file that can be used as parameter when running: ToyRobot.exe <absolute path to toyrobot_input_sample.tx>

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
