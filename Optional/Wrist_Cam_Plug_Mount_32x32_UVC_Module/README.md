# Plug Wrist Camera (MF) Installation Guide for SO-100

<img height="300" src="https://github.com/user-attachments/assets/139be1c3-d446-4304-b0f4-c90a996789d6" />
<img height="300" src="https://github.com/user-attachments/assets/6c2f0f47-9663-4224-ac4e-220d1d71c162" />

## Overview
This guide provides step-by-step instructions for installing a **Wrist Camera** (alternate "McGartoll-Fung" design) on the SO-100 robot using a **Camera Module** and a 3D-printed **Plug-in Camera adapter**.

This an adapatation of [Wrist Camera (MF) UVC Module](../Wrist_Cam_Mount_32x32_UVC_Module/)

## Comparison to Main Design
#### Advantages:
- smaller
- fewer parts
- no additional screws/hardware needed to attach camera
- no removal/replacement of existing pieces
- easy removal/replacement

#### Disdvantages:
- still require to adapt to new camera

## Required Components
### Hardware:
- **USB Camera Module** (1) - this is the [recommended model](https://www.amazon.com/innomaker-Computer-Raspberry-Support-Windows/dp/B0CNCSFQC1/ref=pd_lpo_d_sccl_3/132-7372155-9780230?pd_rd_w=eYz4L&content-id=amzn1.sym.4c8c52db-06f8-4e42-8e56-912796f2ea6c&pf_rd_p=4c8c52db-06f8-4e42-8e56-912796f2ea6c&pf_rd_r=XC3EXZRSSXKDB1G0Z5D7&pd_rd_wg=1wTpn&pd_rd_r=932b1976-9ac7-4cef-9774-f0f9c3acb804&pd_rd_i=B0CNCSFQC1&psc=1), but any 32mm x 32mm USB camera module with min 720p / 30 fps spec will likely work
- [3D-printed Plugin camera attachment](stl/SO-ARM100_Plug_camera.stl) (1)
   - I recommend printing it as oriented in the STL using tree supports. 40% infill is recommended to increase sturdiness and avoid wobbling
- **M2 Screws** (8) - these are the smaller screws that came with your Feetech servos.


<img height="200" alt="Screenshot 2025-03-04 at 7 43 33 PM" src="https://github.com/user-attachments/assets/18099e1d-754c-4877-871f-9113a0dff062" />

## Assembly Instructions
### Step 1: Plug the new camera module to the Gripper
   
2. 3D print the **Plugin camera attachment**.

3. Attach the **Plugin camera attachment**.
    1. The hole fit into the [Gripper hole](../../STEP/Follower_specific/Moving_Jaw_08d%20v1.step)

4. Secure it with the M2 screws




### Step 2: Install the Camera
1. Take out the **Camera Module**.
2. Align the 4 holes of the **Camera Module** with the **Moving Jaw Replacement**, and attach using 4 **M2 Screws**.

<img height="300" src="https://github.com/user-attachments/assets/ea5af652-9311-44c7-8ae8-525f42cb4703" />


### Step 3: Configure Software and Adjust Focus
1. In your software, set your resolution and FPS. 
- **Note**: You will likely want to set your resolution to *640 x 480* and FPS to *30* even if the camera module's max resolution/frame rate is higher, as most models work with lower resolutions and any higher will just be data bloat.
2. Turn on your arm.  Look at the video feed from your newly installed camera (On Mac, you can also use *QuickTime*->*New Movie Recording* to see this feed).  
- **Note**: The focus on the camera is manual and will look very blurry initially. Adjust the focus by twisting the lens counterclockwise or clockwise until the video feed is clear.
