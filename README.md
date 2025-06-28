# 🛣️ MOG2-Euclidean-Moving-Object-Tracker

This repository hosts a Python-based system for real-time moving object detection and tracking in video streams. It leverages OpenCV's **MOG2** for robust foreground detection and a custom **Euclidean Distance Tracker** for consistent object identification across frames.

---

## ✨ Features

-   🎯 **Object Detection:** Utilizes OpenCV's `BackgroundSubtractorMOG2` to segment moving objects from the background.
-   🚶‍♂️ **Multi-Object Tracking:** Employs a custom `EuclideanDistTracker` to assign unique IDs and track multiple detected objects.
-   🖼️ **Region of Interest (ROI):** Focuses detection and tracking within a specified area of the video frame.
-   🔢 **ID Assignment:** Assigns a unique numerical ID to each tracked object for persistent identification.
-   🖥️ **Real-time Visualization:** Displays the original video, the processed Region of Interest (ROI) with tracking results, and the generated foreground mask.

---

## 🛠️ Requirements

To run these scripts, you'll need Python and the following library:

-   `opencv-python` (for all computer vision operations)

You can install it easily using pip:

```bash
pip install opencv-python
```

---

## 📂 Project Structure

-   `main.py`: The primary script for detecting and tracking moving objects in a video.
-   `tracker.py`: Contains the `EuclideanDistTracker` class, the core logic for object association and ID management.
-   `White Mask.py`: A utility script to demonstrate the `BackgroundSubtractorMOG2` (MOG2) in isolation, showing only the raw foreground mask.

---

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [YOUR_REPO_URL]
    cd MOG2-Euclidean-Moving-Object-Tracker
    ```

2.  **Update Video Paths:**
    * Open `main.py` and `White Mask.py`.
    * Locate the line `cap = cv2.VideoCapture(r"D:\OpenCV\Object-Tracking\highway.mp4")`.
    * **Change this path** to the actual path of your video file (e.g., a highway video, traffic footage, etc.) or `0` to use your webcam.

3.  **Run the main tracking script:**
    ```bash
    python main.py
    ```
    * Press the `Esc` key to exit the video stream.

4.  **To see just the background subtraction mask:**
    ```bash
    python "White Mask.py"
    ```
    * Press the `Esc` key to exit.

---

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improvements, new features, or bug fixes, please feel free to open an issue or submit a pull request.

---

Happy Tracking! 🚗💨
