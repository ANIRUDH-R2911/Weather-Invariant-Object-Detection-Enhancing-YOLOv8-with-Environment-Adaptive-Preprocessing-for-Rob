# Weather-Invariant Object Detection: Enhancing YOLOv8 with Environment-Adaptive Preprocessing for Robust Performance Across Diverse Conditions

This project introduces a weather-adaptive pipeline that integrates a CNN-based weather classifier and targeted image preprocessing with YOLOv8, aiming to improve object detection accuracy under challenging weather conditions like fog, rain, snow, and low light.

## Tech Stack

| Component             | Technology Used                 |
|-----------------------|---------------------------------|
| Object Detection      | YOLOv8                          |
| Weather Classification| CNN (PyTorch)                   |
| Image Preprocessing   | OpenCV, NumPy                   |
| Data Augmentation     | Albumentations                  |
| Evaluation Metrics    | Precision, Recall, mAP          |
| Programming Language  | Python                          |


## Key Features

- **Weather Classification via CNN**  
  Classifies input images into weather types like foggy, rainy, snowy, low-light, etc.

- **Targeted Image Enhancement**  
  Applies preprocessing such as dehazing, gamma correction, and histogram equalization based on the classified weather condition.

- **Robust YOLOv8 Integration**  
  Uses enhanced images to significantly improve object detection performance in challenging weather.

- **Two-Stage Modular Pipeline**  
  Seamless flow from classification to preprocessing to detection, designed for real-world conditions.


## Architecture

```mermaid
graph TD
    A[Input Image] --> B[Weather Classification (CNN)]
    B --> C[Condition-Specific Preprocessing]
    C --> D[YOLOv8 Object Detection]
    D --> E[Detected Objects + Labels]
```


## Dataset
- The folder test contains the test dataset upon which the trained YOLOv8 model and the CNN classifier were tested upon.

- I have provided the original dataset and the augmented dataset so the users may feel free to skip the augmentation part of the code

- Please find below the link to the dataset: [Dataset](https://drive.google.com/drive/folders/1W25B9MSvZd5sKkgoksf7DfyQv7pn5KQy?usp=sharing)

## Results

**Weather Classification (CNN):**
- Training Accuracy: **90.85%**
- Validation Accuracy: **81.84%**
- Test Accuracy: **76%**

**Object Detection (YOLOv8):**
- Precision (P): **0.855**
- Recall (R): **0.874**
- mAP@0.5: **0.931**
- mAP@0.5:0.95: **0.823**

The combined pipeline significantly improves object detection accuracy under adverse weather conditions, demonstrating strong generalization and real-world readiness.


## Future Enhancements

- Add support for extreme weather types like **blizzards** and **sandstorms**
- Include **time-of-day classification** to further adapt preprocessing for night or dusk scenarios
- Integrate **deep learning–based enhancement techniques** (e.g., GANs, transformers)
- Optimize the pipeline for **real-time edge deployment** (e.g., on autonomous vehicles or drones or embedded systems)
- Extend functionality to support **live video stream input** and **batch processing**


## Acknowledgments   
- **Ultralytics YOLOv8** - framework for object detection
- **OpenCV** - for real-time image enhancement
- **Purdue University** – ECE 57000: Artificial Intelligence  

