# Live Facial Expression Detection 😊

## Project Objective

The main goal of this project is to **detect and identify human facial expressions in real-time using a webcam**. It uses artificial intelligence to analyze a person's face and instantly recognize whether they are expressing emotions like happiness, sadness, anger, surprise, fear, disgust, or neutrality. This happens live as you look into your camera!

---

## What Does This Project Do?

Imagine you're sitting in front of your computer, and as you look at your webcam, the program watches your face and tells you what emotion you're expressing right now. That's exactly what this project does! It's like having an emotion reader that works in real-time.

**In simple terms:**
- Your webcam captures video of your face
- The program finds your face in the video
- It analyzes your facial features
- It predicts what emotion you're showing
- It displays the emotion label on your screen with a green box around your face

---

## How It Works (The Simple Explanation)

### Step 1: Face Detection
The program uses a technology called **dlib** to find faces in the video stream. Think of it as a face finder that scans each frame and spots where your face is.

### Step 2: Image Processing
Once it finds your face, it:
- Crops out just your face area
- Converts it to the right size (96x96 pixels)
- Prepares it for the AI model to understand

### Step 3: Emotion Recognition
The AI model (built with **TensorFlow** and **EfficientNetB2**) looks at your face and predicts which of the 7 emotions you're showing:
- 😊 Happy
- 😢 Sad
- 😠 Angry
- 😲 Surprised
- 😨 Fearful
- 🤢 Disgusted
- 😐 Neutral

### Step 4: Display Results
The emotion prediction is shown on your screen with a colored rectangle around your detected face.

---

## Technologies Used

| Technology | Purpose |
|-----------|---------|
| **Python** | Main programming language |
| **TensorFlow** | Deep learning framework |
| **OpenCV (cv2)** | Video capture and image processing |
| **dlib** | Face detection |
| **EfficientNetB2** | Pre-trained neural network for emotion recognition |
| **NumPy** | Numerical operations |
| **Pickle** | Loading trained models |

---

## Project Structure
