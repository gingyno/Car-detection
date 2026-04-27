# Car Detection and Line Crossing Counter

This project utilizes the YOLOv8 object detection model and the Supervision library to track vehicles and count them as they cross a virtual line in a video.

<img width="748" height="375" alt="image" src="https://github.com/user-attachments/assets/e61b81ac-a5ba-4997-9715-cc6eb8de43d8" />


---

## Overview

The application processes a video file to detect specific vehicle classes, tracks their movement across frames using ByteTrack and counts how many unique objects pass a specific coordinate threshold.

### Features
* **Detection:** Powered by YOLOv8n (Nano) for an optimal balance of speed and accuracy.
* **Tracking:** Utilizes ByteTrack to maintain unique identities for vehicles.
* **Class Filtering:** specifically monitors cars, motorcycles, buses, and trucks.
* **Output Generation:** Produces a video file showing car bounding boxes, tracking paths and a total count of crossed cars.

---
### Encountered issues with YOLOv8
* YOLOv8 sometimes has a hard time correctly predicting the right vehicle type. Additionally, the algorithm can label the same car with multiple labels at once. These two separate issues happened simultaneously with a specific car. My guess is that the vehicle is either as large as a small truck or that the bad quality + bad lighting is making the car appear as if it is bigger. 
---
## Technical Requirements

* **Python:** 3.8 or higher
* **Libraries:**
  * `ultralytics`
  * `supervision`
  * `opencv-python`
  * `torch`

Install dependencies via pip:
```bash
pip install ultralytics supervision opencv-python torch
