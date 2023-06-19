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
+ 

+ Displaying a list of running topics
    ```
    rostopic list
    ```

## Graphic display
+ Display the relationships between nodes
    ```
    rpt_graph
    ```
+ Visualize in 3D
    ```
    rviz
    ```

## References
[ROS Tutorials](http://wiki.ros.org/ROS/Tutorials)

## License

© 2023 Yuki NAGAKI