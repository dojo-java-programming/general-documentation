# Dojo Java Assignments


A place for ideas for assignments.


## A World with Actors - Engine

The _World with Actors Engine_ is a small __Engine__, which can create a __World__ and let one or multiple
__Actor__(s) do things in that world.

A concrete implementation would be a _robot_ (__Actor__) that can move around in a _maze_ (__World__) and find the
_exit_ by himself. 

| Actor  | Robot |
| World  | Maze  |
| Engine | Creates a _maze_ and places the _robot(s)_ in the maze. |

The __Engine__ looks over the _maze_ and the _robot(s)_. Each robot has a method __void act()__, in which he can make
decisions what he wants to do.    


## Create Maze Generator

There is this _small explorer robot_ that is keen in searching through complex mazes, for finding the way out.

Create a Maze matrix, for our _explorer robot_, so he has something to do! The maze should contain walls and
open spaces. Like in the sample below.


    XXXXXXXXXX    'X' : Wall element, make sure the square outline is a closed wall.
    X    XX  E    ' ' : Empty space
    X XX XX XX    'E' : The Exit location, which the robot has to find.
    X XX XX XX    '^' : Starting point of the robot, and the director he is facing.
    X        X          | Character | Direction |
    X XXXXXXXX          | '^'       | North     |
    X XX^XX  X          | 'V'       | South     |
    X    XX  X          | '<'       | West      |
    XXXXXXXXXX          | '>'       | East      |


The robot can execute several commands:
- __turn__ _left_ and _right_ (meaning rotating on the current location)
- __move__ _forward_ and _backward_

To let the robot make a decision where he can go, he needs to know where walls and empty spaces are.
For this he can use the command __scan__, which returns what is around him. In front, left, right and behind him. 
