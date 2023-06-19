# ROS Noetic command cheat sheet

This README serves as a cheat sheet for frequently used ROS Noetic commands, specifically designed for beginners.

## File system
+ Change directory to ROS package
    ```
    roscd [package_name]
    ```
    ```
    roscd [package_name]/[subdirectory_name]
    ```
+ List directory to ROS package
    ```
    rosls [package_name]
    ```
    ```
    rosls [package_name]/[subdirectory_name]
    ```

## Execute
+ Start the ROS master
    ```
    roscore
    ```
+ Start the ROS node
    ```
    rosrun [package_name] [node_name]
    ```
    > ROS master needs to be running.
+ Start the ROS launch
    ```
    roslaunch [package_name] [launch_name]
    ```

## Communication information
### **Nodes**
+ Displaying a list of running nodes
    ```
    rosnode list
    ```
+ Displaying detailed information of the specified node
    ```
    rosnode info [node_name]
    ```
    > ex. `rosnode info /rosout`

### **Topics**
+ Displaying topic data
    ```
    rostopic echo [topic_name]
    ```
+ Displaying a list of running topics
    ```
    rostopic list
    ```
+ Displaying detailed information of the specified topic
    ```
    rostopic info [topic_name]
    ```
+ Displaying the update rate of a topic
    ```
    rostopic hz [topic_name]
    ```

### **Services**
+ Displaying available service types
    ```
    rossrv list
    ```
+ Displaying detailed information of the specified service type
    ```
    rossrv show [service_type]
    ```
    > ex. `rossrv show turtlesim/Spawn`
+ Displaying a list of running services
    ```
    rosservice list
    ```
+ Displaying detailed information of the specified service
    ```
    rosservice info [service_name]
    ```
+ Calling the specified service
    ```
    rosservice call [service_name] [args]
    ```
    > ex. `rosservice call /spawn 3 3 0.3 "name"`

### **Params**
+ Displaying available parameters
    ```
    rosparam list
    ```
+ Displaying the specified parameter
    ```
    rosparam get [param_name]
    ```
+ Modifying the specified parameter
    ```
    rosparam set [param_name] [args]
    ```
    > ex. rosparam set background_b 100
    + Reflecting the parameter modifications
        ```
        rosservice call /clear
        ```

## Recording and playback
+ Recording all active topics
    ```
    rosbag record -a
    ```
    > When executed, a bagfile is created in the current directory.
+ Displaying detailed information of the specified bagfile
    ```
    rosbag info [bagfile_name]
    ```
+ Playing back the specified bagfile
    ```
    rosbag play [bagfile_name]
    ```

## Graphic display
+ Visualize in 3D
    ```
    rviz
    ```
+ Display the relationships between nodes
    ```
    rpt_graph
    ```
+ Displaying a time plot of a topic
    ```
    rqt_plot
    ```

## References
[ROS Tutorials](http://wiki.ros.org/ROS/Tutorials)

## License
This project is provided under the [License Name].

Please see the [link to LICENSE file] for details.

© 2023 Yuki NAGAKI