# ROS Noetic command cheat sheet

This README is cheat sheet of frequently used ROS Noetic commands.

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
### **Topic**

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