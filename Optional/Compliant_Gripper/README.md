# Compliant Gripper Guide for the SO-101 Arm

<img src="https://github.com/user-attachments/assets/26de0b8c-8bd6-4651-867f-1358532e2cc6" width="500">

The compliant gripper is a modification of the original rigid gripper that is printed out of a flexible material (TPU). It uses a hollowed-out design with internal ribs to flexibly conform to the objects it grasps, thereby reducing the contact force exerted on the object. This gripper is ideal for objects with difficult geometries or fragile components (e.g., fruit) as it reduces the control precision required to safely manipulate objects. 

## Printing Instructions
The demo compliant gripper was printed with a Bambu Lab printer using a flexible thermoplastic polyurethane (TPU) filament with Shore hardness of 95A. Printer settings included 20% and support generation. The supports were manually removed with flush cutters after printing concluded. 

Not all printers are capable of printing with flexible filaments like TPU. Some printers may require modifications like upgraded printer heads. Printing with TPU may result in longer print times and often requires additional post-processing due to the difficulties in removing the support material. 


## Installation Instructions (SO-101)
No modifications to the robot assembly process or installation are required with the compliant gripper. The external geometry is identical to the original gripper, outside of the removal of some holes and the addition of the cavities/ ribs.

Simply print [Compliant_Moving_Jaw_SO101.stl](stl/Compliant_Moving_Jaw_SO101.stl) and [Compliant_Wrist_Roll_Follower_SO101.stl](stl/Compliant_Wrist_Roll_Follower_SO101.stl) using TPU 95A and install as normal. 

## Further details
This design was created during the June 2025 Hugging Face LeRobot Hackathon by Zach Tabor and Caitlin Freeman from Memphis, TN. The design is loosely inspired from a common compliant gripper design that relies on the Fin Ray Effect&reg;, a concept that was popularized by Festo and used in their compliant grippers. 
