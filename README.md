# oct-dec-majaor-project-IOT
turtlesim_catch_and_catch

Turtlesim
oct-dec majaor project

Turtlesim_CatchAndCatch This is a fun implementation of Catch and Catch game done using ROS Turtlesim.Initially a turtle will be there which is the catcher of the game. A new turtle will be spawned to which the catcher will go to the goal position to catch it. Everytime we catch a turtle a new turtle is spawned in a random position. This process repeats continuously.

image

Flow of program

Locating random positions

Spawning new turtle

Identifying distance

Equating the distance

Killing the turtle

1 . Locating random positions

random.randrange() This function can output a random value between the range of value we give it as a input. So by using this we can locate and spawn a turtle in random positions of the turtlesim workspace.

2 . Spawning new turtle

Turtle_spawn(goal,killer_name,spawn_name) By using this function we can create a new turtle anywhere in the screen according to our inputs. The inputs are goal = position killer_name and spawn_name So the turtle will be spawned at the goal position with the name of spawn_name

3 . Identifying Distance

The distance between the spawned turtle and the catcher turtle is found using the function

euclidean_distance(self, goal_pose)

4 . Equating the distance

Equating the distance between the turtles with the tolerance level, the linear and angular velocities of the turtle is changed simultaneously

while self.euclidean_distance(goal_pose) >= float(distance_tolerance): With that the turtle moves for catching the new turtles

5 . Killing the turtle

Turtle_kill(killer_name) This function is used to kill the turtle whose input parameter is the name of the turtle. Once the catcher turtle catches the newly spawned turtle, then the Turtle_Kill function is been called self.Turtle_kill('turtle2')

Screenshot 2023-03-21 105408
