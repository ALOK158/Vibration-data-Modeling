# Vibration-data-Modeling# Gear Fault Diagnosis using Vibrational Analysis

This project focuses on predictive maintenance for industrial gearboxes by diagnosing faults through the analysis of vibrational data. It implements a machine learning pipeline to classify different gear conditions (e.g., healthy, chipped tooth, worn gear) with the goal of preventing catastrophic failures and reducing operational downtime.

## Table of Contents
- [Overview](#overview)
- [Methodology](#methodology)
- [Dataset](#dataset)
- [Repository Structure](#repository-structure)
- [Technologies Used](#technologies-used)
- [How to Run](#how-to-run)
- [Results](#results)

<img width="625" height="337" alt="image" src="https://github.com/user-attachments/assets/0339efcf-9178-4690-807f-82ca11e6e16c" />
<img width="1024" height="473" alt="image" src="https://github.com/user-attachments/assets/18025450-222f-424f-99e6-a036aa4fc506" />


## Overview
In industrial machinery, gearboxes are critical components whose failure can lead to significant financial loss and safety hazards. This project demonstrates a data-driven approach to fault diagnosis. By capturing and analyzing vibrational signals from a gearbox, we can train a machine learning model to detect and classify faults before they become critical, enabling a proactive, predictive maintenance strategy.

## Methodology
The project follows a standard machine learning workflow:
1.  **Data Acquisition:** Vibrational data was collected from an experimental testbed under various simulated fault conditions.
2.  **Feature Extraction:** **Wavelet Transformation** was used to extract meaningful features from the raw time-series vibration signals. This method is highly effective for analyzing non-stationary signals like those produced by faulty machinery.
3.  **Model Training:** A **Support Vector Machine (SVM)** classifier was trained on the extracted features to distinguish between different health states of the gearbox.
4.  **Evaluation:** The model's performance was evaluated based on its classification accuracy and other relevant metrics.

## Dataset
The dataset used for this project is located in the `/data` folder. It contains time-series vibrational data captured from a gearbox test rig. The data represents various conditions, including a healthy state and several common fault types.

## Repository Structure
├── data/
│   └── (Vibrational data files like .csv, .txt, etc.)
├── gearbox-fault-prediction-svm.ipynb
├── predictive-maintenance-of-gearbox.ipynb
├── edp report final.html
└── README.md

- **`data/`**: Contains the dataset used for training and testing the model.
- **`gearbox-fault-prediction-svm.ipynb`**: The main Jupyter Notebook containing the final implementation of the SVM model, including data loading, preprocessing, feature extraction, training, and evaluation.
- **`predictive-maintenance-of-gearbox.ipynb`**: A Jupyter Notebook likely containing initial exploratory data analysis (EDA), data visualization, and preliminary model testing.
- **`edp report final.html`**: The final project report document, detailing the project's background, methodology, results, and conclusions.

## Technologies Used
- Python 3.x
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
- PyWavelets (or similar library for wavelet transforms)

## How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```
2.  **Install the required libraries:**
    It is recommended to create a virtual environment first.
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You may need to create a `requirements.txt` file by running `pip freeze > requirements.txt` in your project environment).*

3.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
4.  Open the `gearbox-fault-prediction-svm.ipynb` notebook and run the cells.

## Results
The trained Support Vector Machine (SVM) model achieved a **classification accuracy of 80%** in dist
