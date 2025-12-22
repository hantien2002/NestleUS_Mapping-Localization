# NestleUS_Mapping-Localization

## Project Overview

This project focuses on zone localization in industrial environments using vision-based methods.
The goal is to determine which predefined safety or operational zone a person or object belongs to, based on visual input from cameras in a warehouse or factory setting.

The project is organized around multiple localization approaches, starting from image-space methods and extending toward geometry-aware techniques.

### 1. Image-Space Zone Localization (2D)

The image-space approach performs zone localization directly in the 2D image plane.
Zones are defined as regions in the image, and detected objects or people are assigned to zones based on their pixel-level location.

This module focuses on:

- 2D zone definition in image space
- Mapping detections to zones using bounding boxes or keypoints
- Fast deployment without camera calibration or depth information

This serves as the baseline and initial implementation of the project.

### 2. Homography-Based Zone Localization (Future Work)

This approach will use planar homography to map image coordinates to a ground-plane representation.
By projecting detections onto a common plane, zone assignment becomes more geometrically meaningful and camera-independent.

Planned features include:
- Camera calibration and homography estimation
- Image-to-world coordinate mapping
- Ground-plane zone reasoning

### 3. Depth-Based Zone Localization (Future Work)

The depth-based approach will incorporate depth information to perform more accurate spatial localization.
This enables 3D-aware zone reasoning, especially in scenes with elevation changes or occlusions.

Planned features include:
- Depth estimation or depth sensor integration
- 3D localization of detected objects
- Depth-aware zone assignment
