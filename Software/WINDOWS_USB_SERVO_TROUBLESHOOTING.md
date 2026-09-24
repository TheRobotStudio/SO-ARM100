# Windows, USB, and power troubleshooting for SO-101

This guide collects Windows 11 bench results for a standard 7.4 V SO-101 leader/follower pair running LeRobot v0.6.1. It complements the [official LeRobot SO-101 guide](https://huggingface.co/docs/lerobot/so101); use that guide for assembly, calibration, and command syntax.

> [!WARNING]
> Do not use this page to justify an untested electrical configuration. Confirm the voltage rating of every servo, controller, and power supply before connecting it.

## Start with a safe baseline

For the standard 7.4 V configuration, use one appropriate controller and one appropriate power supply for each arm. In the tested setup, a 5 V / 5 A supply powered one arm at a time.

The following setup is **not** a valid baseline:

- two arms sharing one 5 V / 5 A supply: both arms initially connected, but one intermittently lost motor communication after torque activation and movement;
- 12 V follower motors with a 12 V / 2 A supply: this is below the repository's stated 12 V / 5 A+ requirement and was excluded from validation.

The SO-101 leader arm is always 7.4 V. A 12 V supply may only be considered for a compatible 12 V follower configuration, controller, wiring, and power supply.

## Windows serial-port check

Before running LeRobot, connect the controller to the computer using a USB-C **data** cable and check Windows Device Manager.

- A working USB connection should expose a stable serial/COM device.
- A charge-only cable will not expose a usable COM port, and LeRobot cannot connect to the robot through it.
- Cable brand is not the important factor: both Apple and Samsung data-capable USB-C cables worked in the tested setup.
- If a COM port appears and disappears or changes repeatedly, first replace the cable with a known-good data cable before changing motor configuration.

The COM number is assigned by Windows and can differ between computers or connections. Use the port currently displayed by Device Manager in the LeRobot command.

## Tested controller configurations

These are observed results, not a compatibility guarantee for unlisted hardware or wiring.

| Controller | Arm | Motor arrangement | Windows observation | LeRobot observation |
|---|---|---|---|---|
| Seeed Studio Servo Driver Board for LeRobot (SKU 100011625) | Follower | 6 × STS3215 C001, 7.4 V | `USB Serial Device`; stable COM port through reconnects | All six IDs were detected; calibration, torque activation, slow movement, and a short teleoperation check completed without a disconnect or reset. |
| Seeed Studio Servo Driver Board for LeRobot (SKU 100011625) | Leader | 1 × C001, 2 × C044, 3 × C046, 7.4 V | `USB Serial Device`; stable COM port | All six motors were detected; leader calibration completed and the full joint range responded normally. |
| Waveshare Bus Servo Adapter (A) | Follower | 6 × STS3215 C001, 7.4 V | `USB-SERIAL CH340`; stable COM port | All six motors were detected and calibrated; teleoperation worked. Initial connection was slightly slower than with the Seeed board. |
| Waveshare Bus Servo Adapter (A) | Leader | 1 × C001, 2 × C044, 3 × C046, 7.4 V | `USB-SERIAL CH340`; stable COM port | All six motors were detected; calibration completed and the arm operated normally. |

## Connection checklist

1. Power off before changing a controller or USB cable.
2. Use the controller, wiring, motor IDs, and power supply specified for the arm.
3. Connect a known-good USB-C data cable and identify the COM port in Device Manager.
4. Run the calibration or teleoperation command from the [official LeRobot SO-101 guide](https://huggingface.co/docs/lerobot/so101), using that COM port.
5. If LeRobot opens the port but cannot find motors, check the servo bus power, connector seating, motor IDs, and arm configuration before changing software.

For low-level motor diagnostics, the repository's [Debugging Motors](../README.md#debugging-motors) section links to the Feetech software for Windows.
