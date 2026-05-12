# Badminton Pose Prediction 🎯🏸

A real-time badminton pose prediction system built using **Computer Vision**, **MediaPipe**, and **Machine Learning**.  
This project identifies different badminton movements from live webcam input using a simple and lightweight feature extraction approach.

The main goal of this project is to recognize common badminton poses efficiently without relying on complex angle calculations.

---

## 🚀 Features

- Real-time badminton pose prediction
- Uses **MediaPipe** for human pose detection
- Lightweight and efficient feature extraction
- Decision Tree based machine learning model
- Live webcam prediction using OpenCV
- Prediction smoothing using `deque`
- Fast and beginner-friendly implementation

---

## 🧠 Poses Predicted

The model is trained to recognize the following badminton poses:

| Pose | Description |
|---|---|
| **Backhand** | Detects backhand hitting posture |
| **Forehand Defense** | Detects defensive forehand stance |
| **Smash** | Detects powerful overhead smash movement |
| **Stance** | Detects ready position before movement |

---

## ⚙️ Technologies Used

- Python
- OpenCV
- MediaPipe
- Scikit-learn
- NumPy
- Pandas

---

## 📌 Feature Extraction

Instead of using multiple body angles and complex calculations, the final model uses only **3 important features** for prediction:

```python
right_hand_up
right_cross_body
lean_right
```

### Feature Description

| Feature | Purpose |
|---|---|
| `right_hand_up` | Checks whether the right hand is raised |
| `right_cross_body` | Checks whether the right hand crosses the body |
| `lean_right` | Detects body leaning toward the right side |

This simplified approach helped make the model faster, cleaner, and easier to train while still achieving good pose prediction performance.

---

## 🏗️ Project Workflow

### 1️⃣ Dataset Collection
- Collected badminton videos
- Converted videos into image frames

### 2️⃣ Pose Detection
- Used MediaPipe Pose to detect body landmarks

### 3️⃣ Feature Generation
Extracted custom pose features:
- `right_hand_up`
- `right_cross_body`
- `lean_right`

### 4️⃣ Model Training
- Built and trained a Decision Tree model using the generated dataset

### 5️⃣ Live Prediction
- Integrated the trained model with webcam input
- Used `deque` to stabilize predictions and reduce flickering

---

## ▶️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/badminton-pose-prediction.git
```

Move into the project directory:

```bash
cd badminton-pose-prediction
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

### Step 1: Build and Train the Model

Run:

```bash
badminton_model_building.ipynb
```

### Step 2: Start Live Pose Prediction

Run:

```bash
badminton_live.ipynb
```

---

## 📸 Future Improvements

- Add more badminton poses
- Improve model accuracy
- Train with a larger dataset
- Deploy as a web application
- Mobile application support

---

## 🤝 Contributing

Contributions are welcome!

Feel free to fork the repository and submit a pull request.

---

## 📜 License

This project is licensed under the MIT License.

---

## ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub!
