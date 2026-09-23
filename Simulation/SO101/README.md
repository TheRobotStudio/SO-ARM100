# SO101 Robot - URDF and MuJoCo Description

This repository contains the URDF and MuJoCo (MJCF) files for the SO101 robot.

## Overview

- The robot model files were generated using the [onshape-to-robot](https://github.com/Rhoban/onshape-to-robot) plugin from a CAD model designed in Onshape.
- The generated URDFs were modified to allow meshes with relative paths instead of `package://...`.
- Base collision meshes were removed due to problematic collision behavior during simulation and planning.

## Calibration Methods

The MuJoCo file `scene.xml` supports two differenly calibrated SO101 robot files:

- **New Calibration (Default)**: Each joint's virtual zero is set to the **middle** of its joint range. Use -> `so101_new_calib.xml`. 
- **Old Calibration**: Each joint's virtual zero is set to the configuration where the robot is **fully extended horizontally**. Use -> `so101_old_calib.xml`.

To switch between calibration methods, modify the included robot file in `scene.xml`.

## Leader Arm URDF

`so101_leader_new_calib.urdf` is a URDF for the **SO-101 leader** (teleoperation) arm, sharing the "new calibration" zero convention above. It reuses the follower's base/shoulder/upper-arm/lower-arm/wrist links and meshes; only the gripper subtree differs: the fixed follower gripper body is replaced by `Wrist_Roll_SO101.stl` and `Handle_SO101.stl`, and the moving jaw by `Trigger_SO101.stl` (meshes converted from `STEP/SO101/Leader_Specific/`). The actuated joint keeps the name `gripper` for compatibility with the other five arm joints.

```bash
rerun Simulation/SO101/so101_leader_new_calib.urdf
```

**Calibration caveat:** the five arm joints carry the same calibration as `so101_new_calib.urdf`. The trigger joint's zero, travel limits (provisionally 0–45°) and the printed-part inertia estimates were derived from CAD geometry and a rough average printed-part density, not from a measured leader unit — there is no MJCF/XML counterpart yet.

## Motor Parameters

Motor properties for the STS3215 motors used in the robot are adapted from the [Open Duck Mini project](https://github.com/apirrone/Open_Duck_Mini).

## Gripper Note

In LeRobot, the gripper is represented as a **linear joint**, where:

* `0` = fully closed
* `100` = fully open

This mapping is **not yet reflected** in the current URDF and MuJoCo files. 

---

Feel free to open an issue or contribute improvements!
