# pr2_simple_moveit_config
A quick and easy package to use the [MoveIt Motion Planning Framework for ROS](http://moveit.ros.org) with the PR2.

## Installation
1. Clone this repository into your ROS workspace's `src` directory.
2. Navigate to your ROS workspace directory:
   ```bash
   cd /path/to/your/ros/workspace
   ```
3. Use `rosdep` to install dependencies:
   ```bash
   rosdep install --from-paths src --ignore-src -r -y
   ```
4. Build the workspace using `catkin_make`:
   ```bash
   catkin_make
   ```

## Usage
To start the PR2 simulation in Gazebo, run:
```bash
roslaunch pr2_gazebo pr2_empty_world.launch
```

To start MoveIt for PR2, run:
```bash
roslaunch pr2_moveit_config move_group.launch
```

To start RViz with the MoveIt Planning layout, run:
```bash
roslaunch pr2_moveit_config moveit_rviz.launch
```

To start MoveIt Servo, with parameters defined in `config/servo_config.yaml`, run:
```bash
roslaunch pr2_moveit_config arms_servo.launch
```

A simple GUI made with slider_publisher to send Twist commands for MoveIt Servo is also included. To start it, run:
```bash
roslauch pr2_moveit_config arms_servo_twist_sliders.launch
```

For more instructions on other MoveIt tools, please refer to the [MoveIt tutorials](https://ros-planning.github.io/moveit_tutorials/).

## Acknowledgements
This package was originally generated using the [MoveIt Setup Assitant](https://ros-planning.github.io/moveit_tutorials/doc/setup_assistant/setup_assistant_tutorial.html) from [pr2_description](http://wiki.ros.org/pr2_description). Then it was modified and simplified.

## License
This package is distributed under the BSD license. Please see the `LICENSE` file for more details.

## Contributors
- Created by Tony Le ([tonyle98@outlook.com](mailto:tonyle98@outlook.com))