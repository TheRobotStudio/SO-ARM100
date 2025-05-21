# Simulation Models for SO100 and SO101

This folder contains simulation files for the **SO100** and **SO101**.

## SO100

- Contains a single **URDF** file for the SO100 robot.
- You can visualize the URDF using [rerun](https://www.rerun.io/):

```bash
rerun Simulation/SO100/so100.urdf
````

## SO101

- Contains both **URDF** and **MJCF** (MuJoCo) files for simulation.
- You can visualize the available URDF files using rerun:

```bash
rerun Simulation/SO101/so101_new_calib.urdf
rerun Simulation/SO101/so101_old_calib.urdf
```

* For more details on:

  * The differences between the **old** and **new calibration** URDFs.
  * How the **MJCF** file was generated from the CAD model.

👉 See the file [`Simulation/SO101/README.md`](Simulation/SO101/README.md).
