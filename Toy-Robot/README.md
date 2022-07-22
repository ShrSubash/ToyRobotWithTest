<h1> Toy Robot Code Challenge</h1>

<h1> Description: </h1>
The application is a simulation of a toy robot moving on a square tabletop, of dimensions 5 units x 5 units. There are no other obstructions on the table surface.
The robot is free to roam around the surface of the table, but must be prevented from falling to destruction. Any movement that would result in the robot falling from the table must be prevented, however further valid movement commands must still be allowed.
Create an application that can read in commands of the following form:
PLACE X,Y,F MOVE LEFT RIGHT REPORT

. PLACE will put the toy robot on the table in position X,Y and facing NORTH, SOUTH, EAST or WEST.
. The origin (0,0) can be considered to be the SOUTH WEST most corner.
. The first valid command to the robot is a PLACE command, after that, any sequence of commands may be issued, in any order, including another PLACE command. The       application should discard all commands in the sequence until a valid PLACE command has been executed
. MOVE will move the toy robot one unit forward in the direction it is currently facing.
. LEFT and RIGHT will rotate the robot 90 degrees in the specified direction without changing the position of the robot.
. REPORT will announce the X,Y and F of the robot. This can be in any form, but standard output is sufficient.
. A robot that is not on the table can choose to ignore the MOVE, LEFT, RIGHT and REPORT commands.
. Input can be from a file, or from standard input, as the developer chooses.
. Provide test data to exercise the application.

<he>Constrains</h1>
. The toy robot must not fall off the table during movement. This also includes the initial placement of the toy robot.
. Any move that would cause the robot to fall must be ignored.

<h1>Instructions and Valid Commands</h1>
Follow the on screen instructions to place a robot and move it around the board. To exit the application at any time type EXIT (this must be in uppercase)
PLACE X,Y,FACING : This puts the toy on the table in position X,Y and facing NORTH, SOUTH, EAST or WEST. If the toy is already placed, issuing another valid PLACE command will place the toy in the newly specified location.
MOVE : This moves the toy one unit forward in the direction it is currently facing.
LEFT : This rotates the toy 90 degrees to the left (i.e. counter-clockwise) without changing the position.
RIGHT : This rotates toy 90 degrees to the right (i.e. clockwise) without changing the position.
REPORT : This announces the X,Y and direction of the toy by printing to the console.

<h2>Example Input and Output:</h2>

a)----------------
PLACE 0,0,NORTH
MOVE
REPORT
Output: 0,1,NORTH

b)----------------
PLACE 0,0,NORTH
LEFT
REPORT
Output: 0,0,WEST


c)----------------
PLACE 1,2,EAST
MOVE
MOVE
LEFT
MOVE
REPORT
Output: 3,3,NORTH

<h1>Getting the project</h1>
Clone the repository from one of the following locations:

GitHub Link:
 https://github.com/ShrSubash/ToyRobotWithTest/tree/main/Toy-Robot
 
 <h1>Building a Project</h1>
.  Link the the scr and include folder loaction in additional library.
.  Download and install boost library 


<h1>Dependencies</h1>
The project includes headers for the boost libraries. The unit test project can either link statically against the boost unit test framework or use a header only implementation. Conan builds will automatically chose the header only implementation, while a CMake build offers the choice of linking statically.


Get boost at https://www.boost.org/users/download/

For convenience boost includes and Windows static libraries for the unittest framework are provided (Linux to come) in the directory 3rd on the branch win_static_boost_libs. Static boost libraries required are Boost_TEST_EXEC_MONITOR_LIBRARY and Boost_UNIT_TEST_FRAMEWORK_LIBRARY.

<h3>Please check the output folder for more snapshot of the output.</h3>


