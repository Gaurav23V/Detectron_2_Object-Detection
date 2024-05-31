# Object Detection with Detectron2

This repository provides scripts and instructions for performing object detection using the Detectron2 library.

## Introduction

Detectron2 is a high-performance, open-source library developed by Facebook AI Research (FAIR) for object detection, segmentation, and other visual recognition tasks. It provides a comprehensive framework with state-of-the-art models and is built on top of the PyTorch deep learning library.

## Data Preparation

To train an object detection model using Detectron2, you need to organize your data in the following format, which follows the ideal structure for the YOLO library:

    data-dir
    |
    ----- train
    --------- imgs
    ------------ filename0001.jpg
    ------------ filename0002.jpg
    ------------ ....
    --------- anns
    ------------ filename0001.txt
    ------------ filename0002.txt
    ------------ ....
    ----- val
    --------- imgs
    ------------ filename0001.jpg
    ------------ filename0002.jpg
    ------------ ....
    --------- anns
    ------------ filename0001.txt
    ------------ filename0002.txt
    ------------ ....


Additionally, you need a `class.names` file, which contains the names of all the different types of objects in the images.

## Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
2. **Install Requirements**:

    Install the necessary libraries including Detectron2 by running:
   ```bash
   pip install -r requirements.txt
   ```
    To install Detectron2, follow the instructions provided in the <a href = "https://detectron2.readthedocs.io/en/latest/tutorials/install.html">Detectron2 Installation Guide.</a>

3. **Data Directory Update**:

    In the train.py file, update the address of the data directory in the argument parser. 

## Training

- To train your model, run the train.py script. This will start the training process and save a checkpoint of the trained model every 500 iterations. You can modify the checkpoint frequency and other settings in the util.py file.

## Prediction
- For a detailed setup guide and example usage, refer to the reference notebook provided in the repository. Follow along with the notebook to set up your environment and run the scripts effectively.

---
By following these steps, you should be able to train an object detection model using Detectron2 and make predictions on new images. For any issues or questions, feel free to open an issue in this repository. Happy detecting!