# Sports_Performance_Analysis using OpenCV and Centroid Tracking

This project is a Python-based object tracking system that detects and tracks multiple moving people (or objects) in a video using OpenCV. It leverages a simple but effective **Centroid Tracking Algorithm** to assign unique IDs and compute trajectories and speeds for each detected object.

## 📽️ Demo

![Demo](demo.gif) <!-- Replace this with an actual GIF or video if available -->

## 🚀 Features

- Background subtraction with MOG2
- Multi-object tracking with unique ID assignment
- Real-time trajectory plotting
- Speed estimation (in pixels/second)
- Automatic object removal if lost for too long

## 🧠 How It Works

1. **Foreground Detection**: Uses `cv2.createBackgroundSubtractorMOG2` to detect moving objects.
2. **Contour Detection**: Filters out small blobs and calculates centroids.
3. **Tracking**: Maintains a mapping between object IDs and their centroids using a simple distance-based assignment.
4. **Trajectory Drawing**: Tracks the last 32 positions for each object and draws its path.
5. **Speed Calculation**: Computes object speed using frame rate and Euclidean distance between centroids.


## 🛠️ Requirements

- Python 3.6+
- OpenCV
- NumPy

### Install dependencies

```bash
pip install opencv-python numpy

