# Sign Language Detection Model

## Overview

This project presents a real-time Sign Language Detection model built using TensorFlow and OpenCV. The model is trained to recognize a set of Indian Sign Language (ISL) gestures from a live webcam feed, providing a foundation for real-time communication assistance and interactive learning applications.

The core of the system is a deep learning model, a Convolutional Neural Network (CNN) based on a pre-trained **MobileNetV2** architecture. The model was fine-tuned on a custom dataset of 35 classes, including numbers 1-9 and the alphabet letters A-Z. The application captures video from a local webcam, preprocesses each frame, and feeds it into the model to predict the corresponding sign.

## Features

  * **Real-Time Prediction**: The script processes a live video stream from a webcam to make predictions with low latency.
  * **High Accuracy**: The model achieved a **validation accuracy of 99.37%** after training, ensuring robust gesture recognition.
  * **Easy to Use**: A single Python script allows for direct execution on a local machine with a webcam.
  * **Modular Design**: The code is structured to allow for easy swapping of the trained model (`.keras` file) and class labels.
  * **GPU Acceleration**: The model can run on a standard CPU, but performance is significantly improved on a GPU-enabled machine.

## Prerequisites

Before running the application, you need to have the following software installed:

  * **Python 3.x**
  * **pip** (Python package installer)

You will also need to install the required Python libraries.

## Installation

1.  **Create a Virtual Environment (Recommended):**
    A virtual environment keeps project dependencies isolated from your global Python installation.

    ```bash
    python -m venv venv
    ```

2.  **Activate the Virtual Environment:**

      - **On Windows (PowerShell):**
        ```bash
        .\venv\Scripts\Activate.ps1
        ```
      - **On macOS/Linux (Bash/Zsh):**
        ```bash
        source venv/bin/activate
        ```

3.  **Install Required Libraries:**
    Install all necessary packages using `pip`.

    ```bash
    pip install tensorflow opencv-python numpy
    ```

## Usage

1.  **Place Your Model and Labels:**

      - Ensure your trained Keras model file (`.keras` format) is saved in the project directory. The model file is named `arun.keras`.
      - The script requires a list of class labels in the correct order. These labels, which include the numbers '1' through '9' and the letters 'A' through 'Z', are hardcoded into the script.

2.  **Run the Prediction Script:**
    Execute the main Python script from your terminal:

    ```bash
    python sign_language_live_predictor.py
    ```

3.  **Live Prediction:**
    A window will open, displaying the live feed from your webcam. The predicted sign and a confidence score will be overlaid on the video.

4.  **Exit the Application:**
    Press the `'q'` key on your keyboard to close the webcam window and exit the program.
