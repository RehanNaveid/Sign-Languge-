
# Gesture Language Decoder - ASMD  

This document explains the **Architecture**, **Setup**, **Modules**, and **Data Flow** of the **Gesture Language Decoder** project.  

---

## Architecture  

The system consists of several components for data collection, model training, and inference:  
1. **Data Collection**: Uses `collect_imgs.py` and `create_dataset.py` to capture and preprocess gesture images.  
2. **Model Training**: Employs `train_classifier.py` to train a gesture recognition model using the dataset.  
3. **Inference**: Runs `inference_classifier.py` to predict gestures in real-time.  
4. **Pickle Files**:  
   - `data.pickle`: Stores processed dataset information.  
   - `model.p`: Contains the trained model for inference.  

---

## Setup  

### Prerequisites  
Ensure Python 3.8+ is installed.  

### Installation Steps  
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/gesture-lang-decoder.git
   cd gesture-lang-decoder
   ```  

2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```  

3. Collect Gesture Data:  
   Run the script to capture images of hand gestures for dataset creation:  
   ```bash
   python collect_imgs.py
   ```  

4. Create Dataset:  
   Process and structure the collected images into a usable dataset:  
   ```bash
   python create_dataset.py
   ```  

5. Train the Model:  
   Train the gesture classifier on the prepared dataset:  
   ```bash
   python train_classifier.py
   ```  

6. Run the Classifier:  
   Use the trained model for real-time gesture recognition:  
   ```bash
   python inference_classifier.py
   ```  

---

## Modules  

### 1. `collect_imgs.py`  
- Captures images of hand gestures using OpenCV.  
- Saves images for each gesture in separate directories for labeling.  

### 2. `create_dataset.py`  
- Processes the captured images and prepares a dataset.  
- Outputs a serialized dataset file (`data.pickle`) for training.  

### 3. `train_classifier.py`  
- Trains a gesture classification model using the dataset.  
- Saves the trained model as `model.p`.  

### 4. `inference_classifier.py`  
- Loads the trained model (`model.p`) and performs real-time gesture recognition.  
- Displays the predicted gesture alphabet.  

### 5. `requirements.txt`  
- Lists dependencies required for the project, including OpenCV, NumPy, and scikit-learn.  

### 6. `final report.pdf`  
- Documentation of the project’s objectives, methodology, results, and conclusions.  

---

## Data Flow  

1. **Data Collection**  
   - Capture hand gesture images using `collect_imgs.py`.  

2. **Dataset Preparation**  
   - Process and label images into a structured dataset using `create_dataset.py`.  

3. **Model Training**  
   - Train the classification model using `train_classifier.py`.  

4. **Gesture Recognition**  
   - Perform real-time inference using `inference_classifier.py` with the trained model.  

---

## Future Enhancements  

- Add support for recognizing more gestures.  
- Improve model accuracy by collecting larger datasets.  
- Develop a GUI for better user interaction.  

---

End of Document  
