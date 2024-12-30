# Car Counter Project - City and Highway

Welcome to the **Car Counter Project**. This project is designed to count cars in real-time using object detection techniques. It features two main environments for vehicle counting:
- **City Traffic**: Optimized for urban environments with varying traffic conditions.
- **Highway Traffic**: Optimized for highways with continuous traffic flow and fast-moving vehicles.

This project uses **YOLO** (You Only Look Once) for object detection, and it is optimized for **CUDA** and **CDNN** for GPU acceleration to ensure fast and accurate results.

---

### **Overview**

The goal of this project is to detect and count cars in real-time video streams, suitable for both city traffic and highway conditions. The system uses two scripts:
- **City Traffic Mode (`car-counter-city.py`)**: Optimized for urban settings with frequent traffic light changes and pedestrians.
- **Highway Traffic Mode (`car-counter.py`)**: Optimized for detecting fast-moving vehicles on highways.

---

### **Features**
- **Real-Time Car Counting**: Detect and count cars in video streams in real-time.
- **City and Highway Modes**: Specific optimizations for different traffic environments.
- **GPU Acceleration**: Utilizes **CUDA** for fast inference.
- **High Accuracy**: Object detection is performed using the **YOLO** algorithm for high accuracy.
  
---

### **Tech Stack and Requirements**

This project uses several tools and libraries for optimal performance:

#### **Required Libraries**:
Install the following Python libraries:
- **cvzone**: 1.5.6
- **ultralytics**: 8.0.26 (for YOLO models)
- **hydra-core**: >=1.2.0
- **matplotlib**: >=3.2.2
- **numpy**: >=1.18.5
- **opencv-python**: 4.5.4.60
- **Pillow**: >=7.1.2
- **PyYAML**: >=5.3.1
- **requests**: >=2.23.0
- **scipy**: >=1.4.1
- **torch**: >=1.7.0
- **torchvision**: >=0.8.1
- **tqdm**: >=4.64.0
- **filterpy**: 1.4.5
- **scikit-image**: 0.19.3
- **lap**: 0.4.0

#### **System Requirements**:
- **CUDA & GPU Support**: This project uses **CUDA** for GPU acceleration, so you’ll need a compatible NVIDIA GPU and appropriate drivers installed.
- **PyTorch with CUDA**: Ensure that PyTorch is installed with GPU support:
  ```bash
  pip install torch torchvision torchaudio
  ```

---

### **Project Structure**

```bash
Car-Counter/
├── City-Traffic/
│   ├── car-counter-city.py
│   ├── graphics.png
│   ├── mask.png
│   ├── sort.py
│   └── city_traffic_weights.pt
├── Highway-Traffic/
│   ├── car-counter.py
│   ├── graphics.png
│   ├── mask.png
│   ├── sort.py
│   └── highway_traffic_weights.pt
├── __pycache__/
├── README.md
└── requirements.txt
```

---

### **How to Run the Code**

1. **Install Dependencies**:
   First, install all required libraries by running:
   ```bash
   pip install -r requirements.txt
   ```

2. **Choose a Mode**:
   Based on whether you’re working with **City Traffic** or **Highway Traffic**, navigate to the corresponding directory.

   - **City Traffic Mode**:
     ```bash
     cd City-Traffic
     python car-counter-city.py
     ```

   - **Highway Traffic Mode**:
     ```bash
     cd Highway-Traffic
     python car-counter.py
     ```

3. **Input Sources**:
   - For **real-time video** detection, ensure the webcam is connected.
   - For **video files**, place the videos in the respective folder and update the file path in the code.

4. **YOLO Model Weights**: Ensure the correct pre-trained weights (`city_traffic_weights.pt` or `highway_traffic_weights.pt`) are available in the respective folders.

---

### **Project Demonstrations**

#### **City Traffic Mode**

This mode is optimized for urban environments. It handles varying traffic conditions, pedestrians, and frequent traffic signal changes.

![Screenshot 2024-12-30 182400](https://github.com/user-attachments/assets/e3b7f41e-24bd-4b15-88a3-dad6b677a45c)
![Screenshot 2024-12-30 182354](https://github.com/user-attachments/assets/3e9ce0ee-6f45-482e-ae74-ea49c2e8ab9f)


#### **Highway Traffic Mode**

This mode is optimized for fast-moving vehicles and continuous traffic flow, typical of highway settings.

![Screenshot 2024-12-30 180714](https://github.com/user-attachments/assets/313745e3-f2d6-499a-8c7f-12c29611cc7e)
![Screenshot 2024-12-30 180735](https://github.com/user-attachments/assets/ecd12b0c-6ead-4ed5-8100-7d7e1b88a796)
![Screenshot 2024-12-30 180803](https://github.com/user-attachments/assets/f231a8f7-82cf-4d0d-8c3e-1f512bdf0140)


---

### **Car Counter Components**

#### **Key Files:**
- **`car-counter.py`**: Main script for detecting and counting cars on highways. It uses the YOLO model to process the video stream and count cars in real-time.
- **`car-counter-city.py`**: Main script for detecting and counting cars in city traffic conditions. It includes specific adjustments for city environments, such as recognizing pedestrians and slower vehicles.
- **`sort.py`**: A utility script for sorting detected objects and ensuring each car is tracked accurately across frames.
- **`graphics.png`**: A reference image used for graphical representation in the system.

![graphics](https://github.com/user-attachments/assets/dff963f7-03ed-4847-a88d-5d2879f07d45)
![graphics](https://github.com/user-attachments/assets/eac7d51c-6d89-403f-9aec-c3575e436510)

- **`mask.png`**: Used for image processing to identify cars and filter other objects.

![mask](https://github.com/user-attachments/assets/cd37eb7c-39cf-4c82-b8bc-ed9324f44e8e)
![mask](https://github.com/user-attachments/assets/6f12f0b6-d78e-4b01-bd29-83d3305ecc21)

---

### **Contributing**

We welcome contributions to this project! If you'd like to contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Make your changes and test them.
4. Push your changes (`git push origin feature-name`).
5. Open a pull request with a detailed description of your changes.

---

### **License**

This project is licensed under the **MIT License**. 
---

### **Acknowledgments**

- **YOLO**: Special thanks to the creators of the YOLO model for their contributions to object detection.
- **OpenCV**: For handling video input and image processing.
- **PyTorch**: For deep learning model training and GPU acceleration.

---

### **Contact**

If you have any questions or suggestions, feel free to open an issue in the repository or contact me at viditupadhyay07@gmail.com.
