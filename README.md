# AI-Face-Image-Processing

This task was done as a part of competency assesment for an AI internship through Callus Company.
This project uses Python, OpenCV, and Dlib to:

- Detect one or more human faces in an image
- Extract RGB values from key facial landmarks:
  - Left Eye Corner
  - Right Eye Corner
  - Nose Tip
- Save the extracted color data to structured `.csv` files
- Visualize the landmark locations on the image

---

## 📂 Project Contents

- [`AI_Face_Image_Processing.ipynb`](AI_Face_Image_Processing.ipynb) — Main notebook for processing images
- [Sample input images like `face.jpg`](face.jpg) — Example image with one face
- [Sample output CSV files like `face.csv`](face.csv) — RGB values from landmarks

---


## 🧰 Requirements

- Python 3.x
- OpenCV
- Dlib
- Pandas
- Matplotlib

Install required packages using:
pip install opencv-python dlib pandas matplotlib

---

## 📌 Setup Instructions
### 1. Download the Dlib shape predictor model
You can run these commands in the notebook or terminal:

wget http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
bzip2 -d shape_predictor_68_face_landmarks.dat.bz2

### 2. Upload your image files to the working directory

### 3. Run the notebook cells to:
  
  Detect faces
  
  Extract RGB values from facial landmarks
  
  Save results as CSV
  
  Show visual output with landmark annotations

### 4. 📊 Output CSV Format
Each row in the output CSV contains color information from one facial point on one face:

| face_id | region     | x   | y   | R   | G   | B   |
|---------|------------|-----|-----|-----|-----|-----|
| 0       | left_eye   | 100 | 120 | 130 | 120 | 110 |
| 0       | right_eye  | 160 | 120 | 125 | 115 | 105 |
| 0       | nose       | 130 | 150 | 140 | 130 | 120 |
| 1       | left_eye   | ... | ... | ... | ... | ... |
| ...     | ...        | ... | ... | ... | ... | ... |

🧪 Sample Images Included
face.jpg – single face

face_multiple.jpg – multiple faces

nature.jpeg – no face (for error testing)

tiger.jpeg – animal face (for error testing)

These images help you verify both successful and failed detection scenarios.

### 5.❗ Error Handling
The script includes error handling for:

Image file not found or unreadable

No faces detected

Landmark points outside image bounds

Landmark detection failure

It prints appropriate warnings and skips invalid cases.

---

## 📄 License
This project is for educational and research purposes.
The Dlib shape predictor model is distributed under its own license — see http://dlib.net for more details.

---

## 🤝 Acknowledgements
Dlib – for the pretrained 68-point facial landmark model

OpenCV – for face detection and image handling

---
