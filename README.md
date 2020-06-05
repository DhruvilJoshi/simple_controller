# simple_controller
It is a Simple Bot Controller for ROS.

The goal for the robot is to reach the end destination. I subscribe to different nodes and publish them to control the bot. It measures the coordinates in the odometry frame. It works in any unknown environment, of which we are not going to build a map. Than I built a controller that converts the distances from the current position and orientation of the robot into velocity commands that are sent to the /cmd_vel of the robot to make it move towards the location.

If the robots orientation is not towards the target, then it will rotate only the robot until its orientation is towards the target. Once the robot is headed towards the target, just move straight towards the goal until reached, it might turn when there is a turning required to set it towards the goal location. If the robot has minimal collision, it will again orient itself towards the goal location.
