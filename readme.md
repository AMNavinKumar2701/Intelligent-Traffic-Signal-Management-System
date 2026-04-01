# 🚦 Crosswalk Detection System (YOLOv5 + Flask)

This project is a computer vision-based web application that detects pedestrians in a defined crosswalk area from uploaded videos and simulates a traffic signal system.

---

## 📁 Project Structure

project/
│
├── templates/
│   └── upload.html        # Frontend UI for video upload
│
├── uploads/               # Stores uploaded videos
│
├── detect.py              # Main Flask app + detection logic
├── requirements.txt       # Python dependencies
├── environment.yml        # Conda environment config

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
4. YOLOv5 detects objects  on the crosswalks
5. If a person is inside selected rectangle → RED signal  
6. Otherwise → GREEN signal  

---

## 📦 Installation

### Option 1: Using pip (Recommended)

```bash
# Clone repository
git clone <your-repo-url>
cd project

# Create virtual environment
python -m venv venv

# Activate environment (Windows)
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt