# Wrist Camera (MF) Installation Guide for SO-100

<img height="300" src="https://github.com/user-attachments/assets/c3816e51-f116-44f0-aaf8-302b3836c210" />

## Overview
This guide provides step-by-step instructions for installing a **Wrist Camera** (alternate "McGartoll-Fung" design) on the SO-100 robot using a **Camera Module** and a 3D-printed **Jaw Replacement Part**.

## Comparison to Main Design
#### Advantages:
- smaller
- fewer parts
- no additional screws/hardware needed to attach camera

#### Disdvantages:
- requires removal/replacement of existing **Wrist Roll** vs an add-on

## Required Components
### Hardware:
- **USB Camera Module** (1) - this is the [recommended model](https://www.amazon.com/innomaker-Computer-Raspberry-Support-Windows/dp/B0CNCSFQC1/ref=pd_lpo_d_sccl_3/132-7372155-9780230?pd_rd_w=eYz4L&content-id=amzn1.sym.4c8c52db-06f8-4e42-8e56-912796f2ea6c&pf_rd_p=4c8c52db-06f8-4e42-8e56-912796f2ea6c&pf_rd_r=XC3EXZRSSXKDB1G0Z5D7&pd_rd_wg=1wTpn&pd_rd_r=932b1976-9ac7-4cef-9774-f0f9c3acb804&pd_rd_i=B0CNCSFQC1&psc=1), but any 32mm x 32mm USB camera module with min 720p / 30 fps spec will likely work
- [3D-printed Wrist Roll Replacement](Optional/Wrist_Cam_Mount_32x32_UVC_Module/stl/Camera_Holder_Alternate_MF.stl) (1)
- **M2 Screws** (4) - these are the smaller screws that came with your Feetech servos.


<img height="200" alt="Screenshot 2025-03-04 at 7 43 33 PM" src="https://github.com/user-attachments/assets/18099e1d-754c-4877-871f-9113a0dff062" />

## Assembly Instructions
### Step 1: Replace the old [Wrist Roll](../../stl_files_for_3dprinting/Individual/Follower/Print_Follower_SO_ARM100_08k_UP_Prusa%20-%20Wrist_Roll_08c-1.STL) piece with the new one
1. If a [Moving Jaw](../../stl_files_for_3dprinting/Individual/Follower/Print_Follower_SO_ARM100_08k_UP_Prusa%20-%20Moving_Jaw_08d-1.STL) is already installed on the arm, leave it attached. Remove the gripper servo from the existing Wrist Roll piece:
 - unscrewing all 6 of **M3 Screws** from the front and back of the servo attaching it to the Wrist Roll piece 
 - gently pulling the motor out
 - unscrew the remaining 4 **M3 Screws** holding the Wrist Roll piece to the next servo
   
2. 3D print the **Wrist Roll Replacement**.

3. Attach the **Wrist Roll Replacement** by doing the reverse of (1).


### Step 2: Install the Camera
1. Take out the **Camera Module**.
2. Align the 4 holes of the **Camera Module** with the **Moving Jaw Replacement**, and attach using 4 **M2 Screws**.

<img height="300" src="https://github.com/user-attachments/assets/ea5af652-9311-44c7-8ae8-525f42cb4703" />


### Step 3: Configure Software and Adjust Focus
1. In your software, set your resolution and FPS. 
- **Note**: You will likely want to set your resolution to *640 x 480* and FPS to *30* even if the camera module's max resolution/frame rate is higher, as most models work with lower resolutions and any higher will just be data bloat.
2. Turn on your arm.  Look at the video feed from your newly installed camera (On Mac, you can also use *QuickTime*->*New Movie Recording* to see this feed).  
- **Note**: The focus on the camera is manual and will look very blurry initially. Adjust the focus by twisting the lens counterclockwise or clockwise until the video feed is clear.
