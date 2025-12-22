# Image-Space Zone Localization (2D)

This module implements image-space zone localization for industrial scenes.
Zones are defined directly in the 2D image plane, and detected people or objects are assigned to zones based on their pixel-level location.

This approach does not require camera calibration, homography, or depth information, and serves as the baseline localization method for the project.

The main implementation is provided in the notebook `image_space_zone_localization.ipynb`.

## Main Features

- 2D zone definition in image space
- Assignment of detections to predefined zones
- Zone labeling based on bounding box or keypoint position
- Frame-level and video-based processing
- Visualization of zones and localization results

## Expected Folder Structure
The module assumes the following directory structure:
```pgsql
image_space_2d/
├── images/
├── json/
├── image_space_zone_localization.ipynb
└── zones_camera.json
```

## Pipeline Overview

### 1. Define Zones in Image Space
- Define zones as polygons or rectangular regions in pixel coordinates
- Load or manually configure zone layouts for each camera view

### 2. Load Detection Results
- Load detection outputs (e.g., person bounding boxes or keypoints)
- Support for frame-level or video-based detections

### 3. Assign Zones
- Compute representative points (e.g., bottom-center of bounding box)
- Determine zone membership based on image-space location
- Handle edge cases and overlapping zones

### 4. Visualize Localization Results
- Overlay zone boundaries on images or video frames
- Display zone labels for each detected person or object
- Export annotated images or videos

### 5. Frame and Video Processing
- Run zone localization on individual frames
- Process full videos frame-by-frame (future work)
- Save per-frame or per-video localization results (future work)

## Notes

This module operates entirely in the image plane and assumes fixed camera viewpoints.
It is designed as a lightweight and fast baseline before introducing geometry-aware methods such as homography or depth-based localization.

