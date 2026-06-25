# RoadVision Object Detection 🚗🛵

This repository contains the training and inference pipeline developed for the RoadVision_DUET competition. The goal of this project is to accurately detect and classify 13 different types of vehicles commonly found in the dense, chaotic traffic environments of Dhaka, including unique classes like Rickshaws, Tempus, and Agro-use vehicles.

## 🧠 Technical Approach
* **Model:** YOLOv8x (Extra-large) pre-trained weights.
* **Resolution:** High-resolution training at 1280px to capture small objects and distant vehicles in highly occluded scenes.
* **Augmentation Strategy:** Implemented a heavy augmentation pipeline to prevent overfitting on dense traffic:
  * Mosaic (1.0) & Mixup (0.15)
  * HSV adjustments, Fliplr, and Perspective shifts
* **Inference:** Utilized Test-Time Augmentation (TTA) with custom confidence (0.10) and IoU (0.4) thresholds to boost accuracy on the holdout test set.

## 📁 Repository Structure
* `final-notebook_clean.ipynb`: The complete, commented pipeline covering data engineering, formatting, YOLOv8 optimization, and final test-time inference.

## 🚀 Key Learnings
* Transforming unstructured spatial `.csv` data into normalized YOLO bounding box formats.
* Applying computational optimization via gradient descent to tune neural network weights.
* Utilizing Non-Maximum Suppression (NMS) and Intersection over Union (IoU) metrics to balance precision and recall.


## 📖 Behind the Build: Training My First Model

As this was my 1st hackathon or Datathon I wasn't prepared for these things, at first I learned a few things. Then the Competition started and the Problem statement was given. I trained my Low-accurate model with the data and after testing it gave 0.42 score. Then I changed my model to medium and 95 epoch trained that made the score 0.44. 
At the end when just 11 hours was left then I took a bold decision to train a High resolution model and 200 epoch. But the reality was it needed more time but I could manage only 131 epoch and the score was 0.54 with securing a 87th position. Which was a great happiness for me as it was my first hackathon/Datathon. 
Maybe if I was experienced I would knew about the epoch completing time constraint.
