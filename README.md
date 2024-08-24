# 🚗 Automatic Number Plate Recognition System using YOLOv8 🎯

Welcome to the Automatic Number Plate Recognition (ANPR) system built using YOLOv8! This project leverages the power of YOLO (You Only Look Once) for real-time object detection and license plate recognition 🚀. The system is designed to detect vehicles in video frames, extract and recognize the license plates, and store the results for further analysis.

## 📂 Project Structure

Here's a quick overview of the files and their roles:

- **`.gitattributes`**: Configuration file for Git attributes.
- **`add_missing_data.py`**: Script to interpolate missing data for bounding boxes.
- **`main.py`**: Main script that runs the ANPR system, handling video processing, vehicle detection, and license plate recognition.
- **`requirements.txt`**: List of required Python packages for the project.
- **`util.py`**: Utility functions used across the project.
- **`visualize.py`**: Script for visualizing results and bounding boxes on video frames.

## 🛠️ How It Works

### 1. 📦 Model Loading
- The system loads the YOLOv8 model (`yolov8n.pt`) for detecting vehicles and a custom-trained model (`license_plate_detector.pt`) for detecting license plates.

### 2. 🎥 Video Processing
- A video file (`sample.mp4`) is loaded, and frames are processed to detect vehicles and their corresponding license plates.

### 3. 🚗 Vehicle Detection
- Vehicles such as cars and motorcycles are detected using YOLOv8, and their bounding boxes are tracked across frames using the SORT algorithm.

### 4. 🔍 License Plate Detection & Recognition
- Detected vehicles are further analyzed to identify the license plates. The license plates are cropped, preprocessed, and then passed to an OCR model (using EasyOCR) to extract the text.

### 5. 📝 Data Storage
- The recognized license plate data, along with vehicle tracking information, is stored in a CSV file for later analysis.

### 6. 📈 Interpolation of Missing Data
- The `add_missing_data.py` script interpolates any missing bounding box data to ensure smooth tracking of vehicles and license plates across frames.

### 7. 🎨 Visualization
- The `visualize.py` script draws bounding boxes around detected vehicles and license plates in the video, adding the recognized license plate number above each vehicle.

## 🚀 Getting Started

### 1. 🛠️ Installation
To get started, clone the repository and install the required packages:

```bash
git clone https://github.com/himanshudash132/Automatic-Number-Plate-Recognition-system-using-yolov8.git
cd Automatic-Number-Plate-Recognition-system-using-yolov8
pip install -r requirements.txt
```

### 2. 📊 Running the Application
To run the ANPR system on your sample video, execute the following command:

bash
Copy code
python main.py
This will process the video, detect vehicles and license plates, and save the results to test.csv.

### 3. 📈 Visualizing the Results
After processing, you can visualize the results by running:

bash
Copy code
python visualize.py
This will generate an output video with bounding boxes and recognized license plate numbers.



### 🤝 Contributing
Contributions are welcome! If you find any bugs 🐛 or have suggestions 💡 for improvements, feel free to open an issue or submit a pull request.

### 📧 Contact
For any questions or inquiries, feel free to reach out at himanshudash132@example.com 📩. 
