# 🚦 Crosswalk Detection System (YOLOv5 + Flask)

This project is a computer vision-based web application that detects pedestrians in a defined crosswalk area from uploaded videos and simulates a traffic signal system.

---

## 📁 Project Structure

project/
│
├── templates/
│ └── upload.html # Frontend UI for video upload
│
├── uploads/ # Stores uploaded videos
│
├── detect.py # Main Flask app + detection logic
├── requirements.txt # Python dependencies
├── environment.yml # Conda environment config

---

## ⚙️ Features

- Upload video through web UI  
- Detect people using YOLOv5  
- Draw crosswalk region manually  
- Traffic signal simulation:
  - 🔴 Red → Person detected  
  - 🟢 Green → No person  
- Real-time frame processing with OpenCV  

---

## 🧠 How It Works

1. User uploads a video from UI  
2. Video is saved in `uploads/`  
3. OpenCV reads frames  
4. YOLOv5 detects objects  
5. If a person is inside selected rectangle → RED signal  
6. Otherwise → GREEN signal  

---

## 📦 Installation

### Option 1: Using pip (Recommended)

```bash
git clone <your-repo-url>
cd project
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

### Option 2: Using Conda

```bash
conda env create -f environment.yml
conda activate traffic
```

---

## ▶️ Run the Application

```bash
python detect.py
```

Open your browser and go to:
http://127.0.0.1:5000

---

## 🎯 Usage Instructions

1. Open the web app  
2. Upload a video  
3. Draw a rectangle (crosswalk area)  
4. Detection:
   - Person inside → 🔴 Red Light  
   - No person → 🟢 Green Light  
5. Press **q** to exit  

---

## 🛠️ Technologies Used

- Python  
- Flask  
- OpenCV  
- PyTorch  
- YOLOv5  
- HTML/CSS  

---

## ⚠️ Notes

- First run may take time (YOLOv5 model download)  
- GPU recommended for faster processing  

---

## 🚀 Future Improvements

- Save processed video output  
- Automatic crosswalk detection  
- Cloud deployment  
- Real-time webcam support  

---

## 👨‍💻 Author

Your Name
