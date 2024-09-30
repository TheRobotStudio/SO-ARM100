# SO-ARM100
Standard Open Arm 100 - Beta version 1.2

The only components required to build the arm (leader or follower) are the 3d printed parts and the six STS3215 servos (6v or 12v version) plus a single adaptor board to connect to a PC.

Before printing the parts for the arm check the accuracy of your printer by printing a gauge from the stl_parts_for_printing/Gauges folder.

There are two types of gauge, one to check the size of print against standard 4x2 lego block and one against an STS3215 servo:

https://youtu.be/dss8E3DG2rA

The stl files are provided ready to print on many FDM printers with a minimum print area of an Ender 220mm x 220mm or a Prusa/Up with a minimum print area of 205mm x 250mm.

All the parts for the leader or follower are contained in a single file, correctly orientated for z upwards to minimise supports.

Set for supports everywhere but ignore slopes greater than 45 degrees to the horizontal.

There should be no supports in the screw holes with horizontal axes.

Prints tested in PLA with minimal external layers and 20% infill.

Print with 0.4mm nozzle at 0.2mm layers or 0.6mm nozzle at 0.4mm layer.

All the screws needed are provided with the servos themselves.

These can be fastened with a #0 and a #1 Philips screwdriver - both sizes are standard in common precision screwdriver sets.

For the electrical supply, you will also require a 5v or 12v power supply that can drive 4A, or an adjustable laboratory power supply with leads.

For software, any Windows PC can connect over USB to program the servos and run initial tests.

The list of components and tools to buy, assuming you have filament and a working 3d printer already, is:

* 6 x STS3215 Feetech servos - 7.4v or 12v version
* 1 x Waveshare or Feetech FE-URT adaptor board
* 1 x 5v or 12v power supply unit (PSU) or laboratory power supply with leads.
* 1 x 6 piece precision screwdriver set with #0 and #1 crossheads

Feetech sell the 6 servos plus adaptor board here: 

https://www.alibaba.com/product-detail/6PCS-7-4V-STS3215-Servos-for_1600523509006.html?spm=a2747.product_manager.0.0.239671d2ci659e

https://www.alibaba.com/product-detail/6PCS-12V-30KG-STS3215-High-Torque_1601216757543.html?spm=a2747.product_manager.0.0.77a471d201w82i

The Waveshare adaptor board is easier to use than the Feetch FE-URT adaptor board as it is fitted with a standard 5.5mm barrel jack.

https://www.waveshare.com/bus-servo-adapter-a.htm

Detailed video instructions are on the @therobotstudio YouTube channel.

Start with the instructions for programming the servos:

https://youtu.be/fy6Jqq_QaGo?si=xjr0-Jur2sEGA9kf

Then assemble the arm:

https://youtu.be/QkIgxTCq3MY?si=S0YPFFkKXr_Xbh47

There is also a playlist here of the development process: https://www.youtube.com/playlist?list=PLy7gxZH9jzfR0l8fYH8C1nyEc4pxSBrer

The arm is intended for integration with the open source "Le Robot" system being developed by the community at Hugging Face.

Join the project with some of the brightest minds in open AI and robotics development on the discord server at: https://discord.gg/ggrqhPTsMe

Handy URDF viewer here:

https://gkjohnson.github.io/urdf-loaders/javascript/example/bundle/index.html

