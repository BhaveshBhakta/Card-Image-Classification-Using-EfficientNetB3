# Card Image Classification Using EfficientNetB3

## Project Overview

This project focuses on classifying **standard playing cards** using a convolutional neural network with **EfficientNetB3** as the base model. The dataset includes images of cards from **53 distinct classes**, encompassing all suits and ranks, including jokers. The goal is to build a highly accurate classifier that can identify any playing card image.

---

## Technical Highlights

* **Dataset**:

  * 8,154 images representing 53 card types (52 cards + joker)
  * Source: [Kaggle - Cards Image Dataset](https://www.kaggle.com/datasets/gpiosenka/cards-image-datasetclassification)

* **Data Pipeline**:

  * Images are pre-organized into `train`, `valid`, and `test` directories
  * Image paths and labels are mapped into Pandas DataFrames
  * Image augmentation using Keras' `ImageDataGenerator` for robust training

* **Model Architecture**:

  * Base model: **EfficientNetB3** pretrained on ImageNet
  * Additional layers: Flatten → Dense(256) → Dropout → Dense(64) → Dropout → Softmax(53)
  * Freezing EfficientNetB3 layers for efficient transfer learning

* **Training Configuration**:

  * Optimizer: Adam
  * Loss: Categorical Cross-Entropy
  * Epochs: 75
  * Batch size: 40
  * Training and validation accuracy/loss visualized with plots

---

## Purpose and Applications

* **Card recognition systems** for digital casinos and gaming platforms
* Automating **card detection in video feeds or camera input**
* Training base models for **computer vision** in object recognition tasks
* Example of applying **EfficientNetB3 transfer learning** for small custom datasets

---

## Installation

 **Clone the repository**:

   ```bash
   git clone https://github.com/BhaveshBhakta/Card-Image-Classification-Using-EfficientNetB3.git
   cd Card-Image-Classification-Using-EfficientNetB
   ```

---

## Collaboration

We welcome contributions to make this project more powerful and scalable:

* Add **real-time webcam-based prediction**
* Deploy via **Flask or Streamlit app**
* Integrate **custom CNN architectures** or test other EfficientNet variants
* Explore **OCR post-processing** for enhanced card detection in gameplay videos
