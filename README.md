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

Live-Facial-Expression-Detection/
├── Facial_Expression_Recognition.py    # Main script that runs the emotion detector
├── Copy of best_weights.h5             # Trained model weights
├── Copy of LabelEncoder.pck            # Emotion labels converter
└── README.md                           # This file

---

## Getting Started

### Prerequisites
Before running this project, you need to have:
- Python 3.7 or higher installed
- A working webcam
- The required Python libraries

### Installation

1. **Clone the repository:**
   git clone https://github.com/svk154/Live-Facial-Expression-Detection.git
   cd Live-Facial-Expression-Detection

2. **Install required libraries:**
   pip install tensorflow opencv-python dlib numpy

### Running the Project

1. **Update the file paths** in Facial_Expression_Recognition.py:
   - Change the paths on lines 24 and 28 to match where your model files are located on your computer
   
   Example:
   model.load_weights(r"path/to/your/Copy of best_weights.h5")
   pickle_obj = open(rf"path/to/your/Copy of LabelEncoder.pck", "rb")

2. **Run the script:**
   python Facial_Expression_Recognition.py

3. **See it in action:**
   - A window will open showing your webcam feed
   - Your face will be detected and surrounded by a green box
   - Your detected emotion will appear above the box
   - Press Q to quit the application

---

## How to Use

- **See your face detected:** Look at the camera and you'll see a green rectangle around your face
- **Read the emotion:** The emotion label appears above the rectangle (e.g., "Happy", "Sad")
- **Multiple faces:** The program can detect and recognize emotions for multiple faces at once
- **Exit:** Press the Q key to stop the program

---

## Key Features

✅ **Real-time Detection** - Works with your webcam feed instantly  
✅ **Multiple Faces** - Can detect emotions from multiple people at once  
✅ **7 Emotion Classes** - Recognizes 7 different facial expressions  
✅ **Easy to Use** - Simple one-command operation  
✅ **Visual Feedback** - Displays results directly on video  

---

## Model Information

- **Architecture:** EfficientNetB2 (a lightweight but powerful AI model)
- **Input Size:** 96 × 96 pixels
- **Output:** 7 emotion classes
- **Framework:** TensorFlow/Keras

The model was pre-trained to recognize facial expressions and can predict emotions with good accuracy.

---

## Possible Use Cases

- 📚 **Education:** Study how facial expressions relate to emotions
- 🎮 **Gaming:** Create games that respond to your emotions
- 💼 **Marketing:** Analyze customer reactions to products
- 🎬 **Content Creation:** Track your expressions while recording
- 🧠 **Research:** Conduct emotion recognition studies

---

## Important Notes

⚠️ **Privacy:** This program only runs on your computer. Your camera feed is not sent anywhere unless you modify the code.

⚠️ **Lighting:** The program works best in good lighting conditions.

⚠️ **File Paths:** You must update the file paths in the code to match your system before running.

⚠️ **Camera Access:** Your system may ask for camera permission the first time you run this.

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| **"No module named 'tensorflow'"** | Run pip install tensorflow |
| **"No module named 'dlib'"** | Run pip install dlib |
| **Camera not working** | Check if your camera is plugged in and allowed by your OS |
| **File not found error** | Update the file paths to where your .h5 and .pck files are actually located |
| **No face detected** | Ensure good lighting and that your face is clearly visible |

---

## License

This project is open source and available for educational and research purposes.

---

## Author

Created by **svk154**

---

## Contributing

Feel free to fork this project and submit improvements! You can:
- Improve the model accuracy
- Add more emotion categories
- Optimize the code for better performance
- Create a better user interface

---

## Questions?

If you have questions about this project, feel free to open an issue on GitHub!

Happy emotion detecting! 😊