
# 🍛 Indian Food Dish Detection using YOLOv8

This project is a real-time food detection and classification system built using the YOLOv8 model. It can detect over **10 unique Indian food dishes** with high precision.

![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)

---

## 📌 Features

- Detects and classifies Indian dishes in real time
- Supports more than 10 unique food categories
- Achieves **80% mean Average Precision (mAP)** on the test set
- Processes images in batches and outputs annotated results
- Fully containerized using Docker with **~10% reduced inference latency**

---

## 🧠 Model Details

- **Model Used**: [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- **Training**: Custom dataset of 3,500+ annotated images
- **Inference**: Fast, optimized detection in production environments
- **Format**: `.pt` model trained and saved in `/model/best.pt`

---

## 🗂 Directory Structure

```
project/
├── model/
│   ├── best.pt            # Trained YOLOv8 model
│   ├── images/            # Folder with input images
│   └── output/            # Folder where output images will be saved
├── detect.py              # Main inference script
└── README.md              # Project overview
```

---

## 🔧 Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-repo/indian-food-detector.git
   cd indian-food-detector
   ```

2. **Install Dependencies**
   ```bash
   pip install ultralytics pillow
   ```

3. **Place Images**
   - Add your `.jpg`, `.jpeg`, or `.png` images to the `/model/images` directory.

4. **Run Detection**
   ```bash
   python detect.py
   ```

   Output images will be saved to `/model/output`.

---

## 🐳 Docker Support

To run the project inside a Docker container:

**Dockerfile**
```dockerfile
FROM python:3.9

WORKDIR /app

COPY . /app

RUN pip install ultralytics pillow

CMD ["python", "detect.py"]
```

**Build and Run**
```bash
docker build -t food-detector .
docker run -v $(pwd)/model:/model food-detector
```

---

## 🧪 Results

- **Test Set Size**: ~500 images
- **mAP@0.5**: ~80%
- **Latency**: Reduced by ~10% post Docker optimization
- **Inference Speed**: Real-time (depending on GPU/CPU)

---

## 📷 Sample Classes Detected

- Chicken Tikka
- Dosa
- Paneer Butter Masala
- Samosa
- Chole Bhature
- Biryani
- Idli
- Vada Pav
- Rajma Chawal
- Gulab Jamun

---

## 📚 Technologies Used

- Python
- Ultralytics YOLOv8
- OpenCV / Pillow (for image I/O)
- Docker (for containerization)
- PyTorch

---

## ✍️ Author

**Devansh Shukla**  
Feel free to connect on [LinkedIn](https://www.linkedin.com/in/devansh-shukla-098b06230/)
