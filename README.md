# Galaxy Image Classifier

**Research Period:** April 2024 – May 2024  
**Goal:** Classify galaxies based on shape using SDSS survey data and a custom neural network built in **PyTorch**.

---

## Table of Contents
- [Introduction](#introduction)
- [Key Results](#key-results)
- [Project Structure](#project-structure)
- [Dependencies & Installation](#dependencies--installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Data](#data)
- [Future Work](#future-work)
- [References](#references)
- [License](#license)

---

## Introduction

**Problem:** Existing shape-based galaxy classification methods struggle with high-volume catalogs (e.g., from SDSS), making it hard to accurately categorize galaxies on a large scale.

**Solution:** We developed a custom **PyTorch** model to classify galaxies based on their morphological features, achieving significant improvements in accuracy and reliability. The approach reduces manual intervention and better handles the extensive variety of galaxy shapes in large catalogs.

---

## Key Results

- **RMSE < 0.11**: Demonstrates strong predictive capability for galactic shape and interaction conditions.  
- **High Scalability**: Model can handle large-scale data from SDSS without a significant drop in accuracy.  
- **Robust Custom Neural Network**: Tailored architecture effectively recognizes morphological differences in galaxy images.

---

## Project Structure

- **Classifier_Main.ipynb**  
  Main Jupyter notebook containing code for data loading, model training, and evaluation.
  
- **custom_model.pth**  
  Trained PyTorch model weights (Custom neural network).

- **training_classifications (1).csv**  
  Example classification results or labeled data used for training validation.

- **clear_structure (1).png / smooth_structure (1).png**  
  Example images or references showing morphological distinctions in galaxies.

- **The_Galaxy_Image_Classifier.pdf**  
  Project paper or detailed report describing methodology, experiments, and results.

- **README.md**  
  This file—overview and instructions.

---

## Dependencies & Installation

1. **Clone this Repository**  
   ```bash
   git clone https://github.com/your_username/Galaxy-Image-Classifier.git
   cd Galaxy-Image-Classifier
   ```

2. **Install Python Packages**  
   ```bash
   pip install -r requirements.txt
   ```
   Packages may include:
   - **PyTorch** (for the neural network)
   - **torchvision** (for transforms / image loading)
   - **numpy**, **pandas**, **matplotlib** (for data handling and visualization)

3. **(Optional) Set Up a Virtual Environment**  
   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

---

## Usage

1. **Jupyter Notebook**  
   - Open **Classifier_Main.ipynb** in Jupyter or VSCode, and run the cells step by step.  
   - This notebook loads galaxy images, processes them, trains the neural network, and evaluates the results.

2. **Training & Evaluation**  
   - Adjust hyperparameters (like `batch_size`, `learning_rate`, `num_epochs`) in **Classifier_Main.ipynb**.  
   - **custom_model.pth** can be replaced or retrained if you make changes.

3. **Data Source**  
   - SDSS Survey images are required. Update paths in the notebook to point to your local copy of the dataset or specify the remote location if using direct downloads.

---

## Model Architecture

1. **Custom Convolutional Layers**  
   - Extract morphological features (e.g., spiral arms, bulges, elliptical halos).  
2. **Fully Connected Layers**  
   - Classify galaxy shape categories based on extracted features (e.g., spiral, elliptical, irregular).  
3. **Loss & Optimization**  
   - Typically uses cross-entropy or MSE (depending on the final label encoding).  
   - Optimizer: e.g., Adam with a set learning rate schedule.

---

## Data

- **SDSS Survey**: Large-scale galaxy images used for training and testing.  
- **Training Labels**: Galaxy shape or morphological class.  
- **Example CSV**: `training_classifications (1).csv` referencing image file paths and their true labels.

Ensure you respect SDSS data usage policies and licenses.

---

## Future Work

- **Expand Morphology Categories**: Include finer sub-classes (e.g., barred spirals, ring galaxies).  
- **Transfer Learning**: Utilize pretrained CNNs (e.g., ResNet, VGG) to improve accuracy.  
- **Active Learning**: Dynamically add new labeled data to retrain the model on challenging cases.  
- **Deployment**: Wrap the model in a web service or cloud platform (e.g., AWS SageMaker) for broader usage.

---

## References

- **SDSS**: [Sloan Digital Sky Survey](https://www.sdss.org/)  
- **PyTorch**: [PyTorch Official Docs](https://pytorch.org/)
- **Galaxy Zoo Image Set**: [Training Set](https://data.galaxyzoo.org/)
---

## License

This project is licensed under the [MIT License](LICENSE). Feel free to modify and adapt for your galaxy classification needs.
