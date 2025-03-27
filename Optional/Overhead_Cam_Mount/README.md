# Overhead Camera Installation Guide for SO-100


## Overview
This guide provides step-by-step instructions for installing a **Overhead Camera** on the SO-100 robot using a **Web Camera** and a 3D-printed **Arm Base and Camera Mount**.

## Design Goals

Design Aims:
1. To create camera data which can be used as model input, either by itself or in conjunction with wrist camera(s) footage.
2. To provide a camera that can provide a overhead view of the entire manipulation space.
3. To make this camera usable as-is in the two most popular configurations, either in a single follower arm setup, or a double follower ("bi-manual") arm setup.


## Required Components
- **Web Camera** (1) - this is the [recommended model](https://www.amazon.com/dp/B082X91MPP)
- 3D-printed parts
    - [Arm Base](stl/arm_base.stl) (1)
    - [Camera Mount Bottom](stl/cam_mount_bottom.stl) (1)
    - [Camera Mount Top](stl/cam_mount_top.stl) (1)
- **M2 Screws** (8) - these are the smaller screws that came with your Feetech servos.


<img height="200" alt="Screenshot 2025-03-04 at 7 43 33 PM" src="https://github.com/user-attachments/assets/18099e1d-754c-4877-871f-9113a0dff062" />

## Assembly Instructions
### Step 1: Remove the existing base from the *webcam*
### Step 2: Attach the *webcam* onto the *camera mount top*
### Step 3: Attach the *camera mount top* to the *camera mount bottom*.
### Step 4: Attach the *arm base* to the *camera mount bottom*.
### Step 5: Attach the *SO-100 follower arm* to the *arm base*.

### Step 6: Configure Software 
1. In your software, add your overhead cam, including setting its resolution and FPS. 
- **Note**: You will likely want to set your resolution to *640 x 480* and FPS to *30* even if the camera module's max resolution/frame rate is higher or wider, as most models work with lower resolutions and any higher will just be data bloat.  This camera mount was specifically designed for 640 x 480 resolution and width.
2. Look at the video feed from your newly installed camera (On Mac, you can also use *QuickTime*->*New Movie Recording* to see this feed).  You should be able to see the workspace of the arm(s).

## Acknowledgements

- Conor McGartholl
    - Design and R & D
- Philip Fung
    - R & D