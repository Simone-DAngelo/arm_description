# arm_description
This package contains a 6 DoFs manipulator model to simulate with Gazebo. The model is included in the [mav_description](https://github.com/Simone-DAngelo/mav_description)/launch/ndt2_with_arm.launch file.

You can control each joint with a std_msgs/Float64 message on the following topics:

    /Rev3_position_controller/command
    /Rev4_position_controller/command
    /Rev5_position_controller/command
    /Rev6_position_controller/command
    /Rev7_position_controller/command
    /Rev8_position_controller/command
 
To get information from the manipulator you can use the following topic:
  
    /joint_states

The manipulator is equipped with a force sensor on its End-Effector to measure the interaction with the environment. These measures are published in the following topic:

    /ndt2/ft_sensor

When a contact is detected the actual interaction force is stored in a /gazebo_msgs/ContactsState message.



