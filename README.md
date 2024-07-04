# SO-ARM100
Standard Open Arm 100 - Early alpha for testing prints and sizings, all the prints are correctly orientated for z upwards to minimise supports.

The only components required to assemble the arm are the 3d printed parts and the six STS3215 servos with a single FE-URT adaptor board.

All the screws needed are provided with the servo. These can be fastened with a #0 and a #1 Philips screwdriver. Both sizes are standard in common precision screwdriver sets.

For the electrical supply, you will also require a 6v power supply that can drive 4A, or an adjustable laboratory power supply with leads.

For software, any Windows PC can connect over USB to program the servos and run initial tests.

The list of components and tools to buy, assuming you have filament and a working 3d printer already, is:

6 x STS3215 Feetech servos
1 x FE-URT adaptor board
1 x 6 piece precision screwdriver set
1 x wire cutters
1 x 6v power supply unit (PSU) or laboratory power supply with leads.

The stl files for the 3d printed parts are in the /parts folder in three sub folders.

3dprint a single copy of the three parts in /part/arm and 3dprint a single copy of the two parts in /parts/base for a total of five 3dprinted parts.

There are several versions of the jaws in the /part/jaws folder, one each of the Wrist_Roll_x.STL and one each of the Moving_Jaw_x.STL should be 3d printed.

The jaw parts are designed in pairs:

Moving_Jaw_b.STL is paired with Wrist_Roll_e.STL
Moving_Jaw_c.STL is paired with Wrist_Roll_f.STL
Moving_Jaw_f.STL is paired with Wrist_Roll_g.STL

If required for finer work, extra tips that can be screwed to the jaws with surplus screws from the servos are available in /parts/jaws/removable_jaws. Choose as required.

The 3d printing settings should be for no supports for angles greater than 45 to the horizontal and no supports for areas under 3mm2.

13% infill and 2 surface layers works well in high performance materials and probably fine for all materials due. We will soon test and confirm for common materials like PLA and Silk PLA.

Detailed video instructions are on the @therobotstudio YouTube channel.

Start with the instructions for programming the servos:

https://youtu.be/fy6Jqq_QaGo?si=xjr0-Jur2sEGA9kf

Then assemble the arm:

https://youtu.be/QkIgxTCq3MY?si=S0YPFFkKXr_Xbh47

There is also a playlist here of the development process: https://www.youtube.com/playlist?list=PLy7gxZH9jzfR0l8fYH8C1nyEc4pxSBrer

The arm is intended for integration with the open source "Le Robot" system being developed by the community at Hugging Face.

Six STS3215 servos are needed to actuate the five dof in the arm and the gripper connected via one adaptor board.

No other components except a PC and power supply with leads.

Simple hand tools only and takes under an hour to assemble to first movements.

At quantities of 1000 units even the higher power 12v version of the STS3215 servos used in all the joints of the present arm design are under 12 USD each - exworks - so around 15 USD in your hand.

Plus an adaptor board to connect to a computer and a clamp to fix it the desk.

If 167 (1000/6 = 166.6666) people are all prepared to buy the servos at once, and assuming that everything else is 3d printed, that's a 5DOF arm with gripper (6 dof total) and a half kilo payload for 100 bucks.

Join the project with some of the brightest minds in open AI and robotics development on the discord server at: https://discord.gg/TBDKjzuX


## Jaws
30mm wide tips - Wrist_Roll_05f and Moving_Jaw_04c
