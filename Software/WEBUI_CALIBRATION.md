# WebUI 3-Point Calibration Studio Guide for SO-ARM100 / SO-101

This guide details how to use the interactive **WebUI 3-Point Calibration Studio** for calibrating Feetech STS3215 serial bus servos on the SO-ARM100 and SO-101 follower arms.

---

## 🌟 Why Use WebUI Calibration?

Traditional hand-held midpoint calibration requires manually holding all 6 joints in mid-air simultaneously. This introduces position errors (±50–200 ticks per joint) and can drive Motor 3 (`elbow_flex`) into hardstop collisions (~3660 ticks).

The **WebUI Calibration Studio** fixes this by providing:
1. **Interactive 3-Point Calibration**: Capture `📍 Min`, `🏠 Home`, and `📍 Max` independently per joint.
2. **Single-Servo Isolation**: Moves only one target joint while holding the other 5 servos securely at their current positions.
3. **Safe Torque Limits**: Applies a **30% torque cap** (`Reg 48 = 300`) and smooth 50Hz cosine S-curve speed interpolation to prevent gear stripping and sudden snaps.
4. **Instant Telemetry**: Live position feedback directly in your browser.
5. **Safe File Updates**: Updates `follower.json` cleanly on disk without deleting existing calibration history.

---

## 🚀 Step-by-Step Instructions

### Step 1: Launch the Calibration Studio
On your host computer (Raspberry Pi, Linux, macOS, or Windows) connected to your arm via USB:

```bash
python pi_servo_studio.py
```
*(Or when using LeRobot integration: `lerobot-calibrate --robot.type=so101_follower --webui`)*

Open your browser and navigate to:
```
http://localhost:8086
```

---

### Step 2: Calibrate Each Joint (3-Point Workflow)

For each motor (`1` through `6`):

1. **Select Joint**: Click on the joint name (e.g., `Motor 3 - Elbow Flex`).
2. **Set Min Limit (`📍 Capture Min`)**:
   - Manually guide or jog the joint to its physical minimum endstop.
   - Click **`📍 Capture Min`**.
3. **Set Home Position (`🏠 Capture Home`)**:
   - Move the joint to its default tucked/resting posture.
   - Click **`🏠 Capture Home`**.
4. **Set Max Limit (`📍 Capture Max`)**:
   - Move the joint to its physical maximum endstop.
   - Click **`📍 Capture Max`**.

---

### Step 3: Verify & Save

1. Click **`Safe Test Home`** to test joint movement at 30% torque limit.
2. Click **`Save Calibration`** to update `follower.json`.

---

## 🛡️ Safety Systems Built-In

- **Torque Cap**: Enforces 30% maximum PWM torque limit ($300 / 1000$).
- **S-Curve Interpolation**: Cosine velocity profile eliminates initial movement jerks:
  $$lpha = rac{1 - \cos(\pi t / T)}{2}$$
- **Serial Buffer Reset**: Flushes UART input/output buffers before every command to prevent stale byte echoes over half-duplex serial bus (`/dev/ttyACM0`).
