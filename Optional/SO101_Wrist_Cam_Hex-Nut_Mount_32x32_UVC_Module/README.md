# Hex-Nut Recess Wrist Camera (MF) Installation Guide for SO-101

<img width="300" src="https://github.com/user-attachments/assets/ef919565-230d-43b4-8363-feb26f23967c" />
<img width="300" src="https://github.com/user-attachments/assets/ae01ce6a-a953-4787-b792-7a17e8091094" />

## Overview
This guide provides step-by-step instructions for installing a **Wrist Camera** (alternate "McGartoll-Fung" design) on the SO-101 robot using a **Camera Module** and a 3D-printed **Hex-Nut Recess Camera Adapter**.

This adapts the [Wrist Camera (MF) UVC Module](../Wrist_Cam_Mount_32x32_UVC_Module/) and [Wrist Camera (MF) UVC Plug‑on Module](../Wrist_Cam_Mount_32x32_UVC_Module/).

## Comparison to Main Design
#### Advantages:
- adapted to use the hex-nut recesses on the wrist of the SO-101 follower arm

#### Disadvantages:
- still requires adaption to the new camera
- requires two screws and two nuts which are not included with the servos
- not backwards-compatible to the SO-100

## Required Components
### Hardware:
- **USB Camera Module** (1) - this is the [recommended model](https://www.amazon.com/innomaker-Computer-Raspberry-Support-Windows/dp/B0CNCSFQC1/ref=pd_lpo_d_sccl_3/132-7372155-9780230?pd_rd_w=eYz4L&content-id=amzn1.sym.4c8c52db-06f8-4e42-8e56-912796f2ea6c&pf_rd_p=4c8c52db-06f8-4e42-8e56-912796f2ea6c&pf_rd_r=XC3EXZRSSXKDB1G0Z5D7&pd_rd_wg=1wTpn&pd_rd_r=932b1976-9ac7-4cef-9774-f0f9c3acb804&pd_rd_i=B0CNCSFQC1&psc=1), but any 32mm x 32mm USB camera module with min 720p / 30 fps spec will likely work
- [3D-printed Hex-Nut Recess Camera Adapter](stl/SO-ARM101_camera_wrist_mount.stl) (1)
   - I recommend printing it as oriented in the STL using tree supports. 40% infill is recommended to increase sturdiness and avoid wobbling
- **M2 Screws** (4) - these are the smaller screws that came with your Feetech servos.
- **M3 x 8mm Screws** (2)
- **M3 Hex Nuts** (2)


<img height="200" alt="Screenshot 2025-03-04 at 7 43 33 PM" src="https://github.com/user-attachments/assets/18099e1d-754c-4877-871f-9113a0dff062" />

## Assembly Instructions
### Step 1: Attach the Adapter to the Gripper
   
1. 3D print the **Hex-Nut Recess Camera Adapter**.

2. Remove Motor 6, you can leave the [Moving Jaw](../../STL/SO101/Individual/Moving_Jaw_SO101.stl) attached.

3. Insert the hex nuts into the recesses in the [Wrist Roll Element](../../STL/SO101/Individual/Wrist_Roll_Follower_SO101.stl).

<img width="300" src="https://github.com/user-attachments/assets/68f34831-eeb1-4e90-83a2-4e204a94ac51" />

4. Reattach Motor 6, secure it with its original M2 screws again.

5. Secure the adapter with the two M3 screws.



### Step 2: Install the Camera
1. Take out the **Camera Module**.
2. Align the 4 holes of the **Camera Module** with the **Camera Adapter**, and attach using 4 **M2 Screws**.

<img width="300" src="https://github.com/user-attachments/assets/baea05ba-2865-4d41-8a53-0ca6ef2b73fe" />


### Step 3: Configure Software and Adjust Focus
1. In your software, set your resolution and FPS. 
- **Note**: You will likely want to set your resolution to *640 x 480* and FPS to *30* even if the camera module's max resolution/frame rate is higher, as most models work with lower resolutions and any higher will just be data bloat.
2. Turn on your arm.  Look at the video feed from your newly installed camera (On Mac, you can also use *QuickTime*->*New Movie Recording* to see this feed).  
- **Note**: The focus on the camera is manual and will look very blurry initially. Adjust the focus by twisting the lens counterclockwise or clockwise until the video feed is clear.
