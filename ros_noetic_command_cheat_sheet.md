# ROS Noetic command cheat sheet

This document serves as a cheat sheet for frequently used ROS Noetic commands, specifically designed for beginners.

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
    rqt_graph
    ```
+ Displaying a time plot of a topic
    ```
    rqt_plot
    ```

## License

<a rel="license" href="http://creativecommons.org/licenses/by/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/3.0/88x31.png" /></a><br />This document is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/3.0/">Creative Commons Attribution 3.0 Unported License</a>.

It has been created with reference to the [original document](http://wiki.ros.org/ROS/Tutorials), and we express our gratitude to the original document's author(s) for their contribution.

© 2023 Yuki NAGAKI