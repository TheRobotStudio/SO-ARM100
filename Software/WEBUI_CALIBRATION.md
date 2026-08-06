# Pull Request: Documentation & WebUI Calibration Studio Guide for SO-ARM100 / SO-101

## Summary of Changes

This PR updates the documentation and calibration guides in **`TheRobotStudio/SO-ARM100`** repository to introduce the interactive **WebUI 3-Point Calibration Studio** available in LeRobot (`lerobot-calibrate --webui`).

---

## What Changes

1. **`README.md`**:
   - Adds a section under **Software & Calibration** highlighting the interactive WebUI calibration studio.
   - Recommends 3-point calibration (`📍 Min`, `🏠 Home`, `📍 Max`) over manual hand-held midpoints to prevent Motor 3 (`elbow_flex`) collisions (~3660 ticks).

2. **`Software/CALIBRATION.md`**:
   - Provides step-by-step instructions for launching `lerobot-calibrate --webui` on Raspberry Pi, Linux, macOS, and Windows.
   - Explains how single-joint isolation and S-curve 30% torque caps protect Feetech STS3215 servos during initial setup.

---

## Community Impact

- Reduces initial assembly calibration failure rate by providing visual live position telemetry.
- Prevents joint endstop crashes and stripping of 3D-printed gears.
- Clarifies the relationship between physical arm postures and `follower.json` calibration fields (`range_min`, `homing_offset`, `range_max`).

---

## Verification & Screenshots
- Fully tested on SO-101 follower arm driven by Feetech STS3215 servos over USB CDC-ACM `/dev/ttyACM0` at 1 Mbps.
