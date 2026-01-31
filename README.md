# 📸 Better Boyfriend

**The AI-powered camera assistant that saves relationships, one photo at a time.**


## 📖 Overview

**Better Boyfriend** is a computer vision web application designed to solve a universal problem: bad photos taken by reluctant partners. 

Unlike standard camera apps that just provide a grid, this application uses **Real-Time Edge AI** to actively "coach" the photographer. It tracks the subject's skeleton in 30fps, compares it against professional pose templates, and provides granular, real-time feedback (e.g., "Tilt Down," "Step Back," "Perfect") to ensure the perfect shot.

## 🚀 Live Demo
Try the latest build on your mobile device:
**[https://betterboyfriend.netlify.app](https://betterboyfriend.netlify.app)**

> **Note:** Please allow camera permissions when prompted. The AI runs entirely locally on your device for privacy.

---

## ✨ Features

* **Real-Time Skeletal Tracking:** Detects 33 distinct body landmarks (nose, wrists, hips, ankles) instantly using the front or back camera.
* **"Traffic Light" Feedback System:**
    * 🔴 **Red:** Subject not found.
    * 🟡 **Yellow:** Subject detected but pose is incorrect (e.g., "Too close," "Headroom issue").
    * 🟢 **Green:** Perfect composition.
* **Smart Auto-Capture:** Automatically triggers a 3-second countdown when the perfect angle is held.
* **Guided Poses:**
    * *The Headshot:* Centers facial features.
    * *Tourist Hand:* Ensures hand placement interacts correctly with landmarks.
    * *Full Body (OOTD):* Validates head-to-toe visibility.
    * *Power Pose:* Detects confident body language.

---

## 🛠️ Technical Architecture

This prototype is built as a **Single-Page Application (SPA)** designed for high-performance mobile usage without backend latency.

### The Stack
* **Frontend:** HTML5, Vanilla JavaScript (ES6+).
* **Styling:** Tailwind CSS (via CDN) for rapid, glassmorphic iOS-style UI.
* **Computer Vision:** [Google MediaPipe](https://developers.google.com/mediapipe) (Pose Landmarker Task).
* **Rendering:** HTML5 Canvas API (for skeletal overlays) + SVG (for guide silhouettes).
* **Hosting:** Netlify (Static Edge Hosting).

---

## 💻 Local Installation

To run this project locally on your machine:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/better-boyfriend.git](https://github.com/your-username/better-boyfriend.git)
    ```
2.  **Navigate to the directory:**
    ```bash
    cd better-boyfriend
    ```
3.  **Serve the file:**
    Because this uses the Camera API, it requires a secure context (HTTPS or localhost). You cannot just double-click the HTML file.
    
    *Python 3:*
    ```bash
    python3 -m http.server
    ```
    *VS Code:*
    Right-click `index.html` and select **"Open with Live Server"**.

4.  **Open in Browser:**
    Go to `http://localhost:8000`.

---

## 🔮 Roadmap: Path to App Store

Moving this from a Web Prototype to a fully scalable iOS/Android application involves the following infrastructure evolution:

### Phase 1: Native Wrapper
* **Tech:** React Native or Flutter.
* **Goal:** Wrap existing logic to access native camera controls (focus, exposure) and save directly to Camera Roll.

### Phase 2: Cloud & Backend
* **Auth:** Firebase Auth for user accounts.
* **Database:** Firestore to store custom pose vector data.
* **Storage:** AWS S3 for backing up high-res images.

### Phase 3: Advanced AI
* **Training:** Train custom TensorFlow Lite models on "Instagram-worthy" datasets.
* **Generative AI:** Implement Stable Diffusion API for real-time lighting correction.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Authors

Nitheesh, Sushant, Peeyush Kumar, Alex zhang, Anvesh

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
