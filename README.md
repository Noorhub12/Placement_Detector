# Placement Predictor

This project implements a logistic regression model to predict student placements based on their CGPA and IQ scores. It includes a simple user interface built with `tkinter` that allows users to input CGPA and IQ values and receive predictions.

## Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Hyperparameter Tuning](#hyperparameter-tuning)
- [Saving the Model](#saving-the-model)
- [User Interface](#user-interface)
- [License](#license)

## Overview

The Placement Predictor is designed to help students and educational institutions predict whether a student is likely to be placed based on their academic performance (CGPA) and IQ scores. The project uses logistic regression for the prediction and provides a user-friendly interface for interaction.

## Requirements

- Python 3.x
- numpy
- pandas
- matplotlib
- scikit-learn
- tkinter
- mlxtend
- pickle

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/placement-predictor.git
   cd placement-predictor
   ```

2. Install the required Python packages:

   ```bash
   pip install numpy pandas matplotlib scikit-learn mlxtend
   ```

## Usage

1. Ensure you have the dataset `placement.csv` in the same directory as the script.

2. Run the script to train the model and open the UI:

   ```bash
   python placement_predictor.py
   ```

3. The `tkinter` UI will open. Enter the CGPA and IQ values and click the "Predict" button to see the placement prediction.

## Dataset

The dataset `placement.csv` should have the following structure:

| ID | CGPA | IQ | Placement |
|----|------|----|-----------|
| 1  | 8.0  | 110| 1         |
| 2  | 7.5  | 105| 0         |
| ...| ...  | ...| ...       |

- **ID**: A unique identifier for each student.
- **CGPA**: The CGPA of the student.
- **IQ**: The IQ score of the student.
- **Placement**: The placement status (1 for placed, 0 for not placed).

## Model Training

The logistic regression model is trained using the CGPA and IQ features to predict the placement status. The script splits the data into training and testing sets, scales the features, and trains the model.

## Hyperparameter Tuning

The model's hyperparameters are tuned using Grid Search to find the best combination of `C`, `penalty`, and `solver` parameters. The best parameters found are:

- `C`: 0.1
- `penalty`: l1
- `solver`: liblinear

## Saving the Model

The trained model is saved to a file named `model.pkl` using `pickle` for later use.

## User Interface

The project includes a simple UI built with `tkinter`. Users can enter CGPA and IQ values, and the UI will display the placement prediction.
