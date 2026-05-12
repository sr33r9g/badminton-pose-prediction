# Badminton Pose Prediction 🎯🏸

A real-time badminton pose prediction system using **Computer Vision**, **MediaPipe**, and **Machine Learning**.  
This project detects badminton poses from live webcam/video input using a lightweight feature-based approach.

---

## 🚀 Features

- Real-time pose prediction
- Uses **MediaPipe Pose Detection**
- Lightweight feature extraction
- Decision Tree based classification
- Supports live webcam prediction
- Efficient prediction smoothing using `deque`

---

## 🧠 Poses Detected

The model can predict the following badminton poses:

- Backhand
- Forehand Defense
- Smash
- Stance

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

Instead of using multiple body angles and complex calculations, the final model uses only **3 important features**:

```python
right_hand_up
right_cross_body
lean_right
```

### Feature Description

| Feature | Description |
|---|---|
| `right_hand_up` | Detects whether the right hand is raised |
| `right_cross_body` | Detects whether the right hand crosses the body center |
| `lean_right` | Detects body leaning toward the right side |

This simplified approach improved efficiency and reduced unnecessary complexity.

---

## 🏗️ Project Workflow

### 1️⃣ Dataset Collection
- Collected badminton videos
- Converted videos into image frames

### 2️⃣ Pose Detection
- Used MediaPipe to detect body landmarks

### 3️⃣ Feature Generation
- Extracted custom pose features:
  - `right_hand_up`
  - `right_cross_body`
  - `lean_right`

### 4️⃣ Model Training
- Trained a Decision Tree model using the generated dataset

### 5️⃣ Real-Time Prediction
- Integrated webcam prediction using OpenCV
- Used `deque` for stable predictions

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

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Project

### Step 1: Build the Model

Run:

```bash
badminton_model_building.ipynb
```

### Step 2: Start Live Prediction

Run:

```bash
badminton_live.ipynb
```

---

## 📸 Future Improvements

- Add more badminton poses
- Improve prediction accuracy
- Deploy as a web application
- Mobile application support

---

## 🤝 Contributing

Contributions are welcome!

Fork the repository and submit a pull request.

---

## 📜 License

This project is licensed under the MIT License.

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
