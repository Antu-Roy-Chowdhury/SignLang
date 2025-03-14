# SignLang: Real-Time Sign Language Detection and Translation

**Project Description:**

SignLang is a project dedicated to developing a real-time sign language detector and translator. Leveraging computer vision and machine learning, it aims to bridge communication gaps for individuals who rely on sign language.

**Based on:**

This project builds upon the foundational work provided in [RealTimeObjectDetection](https://github.com/nicknochnack/RealTimeObjectDetection) by nicknochnack.

**Table of Contents:**

* [Installation](#installation)
* [Annotation Setup](#annotation-setup)
* [Project Structure](#project-structure)
* [Usage](#usage)
* [Contributing](#contributing)
* [License](#license)

## Installation

1.  **Clone the Repository:**

    ```bash
    git clone [Your Repository URL]
    cd Tensorflow
    ```

2.  **Create a Virtual Environment (Recommended):**

    ```bash
    python -m venv venv
    venv\Scripts\activate  # On Windows
    source venv/bin/activate # On macOS/Linux
    ```

3.  **Install Dependencies:**

    ```bash
    pip install -r requirements.txt #if you have one, or install them one by one.
    pip install tensorflow
    ```

## Annotation Setup

1.  **Install labelImg:**

    ```bash
    git clone [https://github.com/tzutalin/labelImg](https://github.com/tzutalin/labelImg)
    ```

2.  **Install Required Libraries:**

    ```bash
    pip install lxml
    pip install sip
    pip install PyQt5
    ```

3.  **Navigate to labelImg Directory:**

    ```bash
    cd labelImg
    ```

4.  **Compile Resources:**

    ```bash
    pyrcc5 -o libs/resources.py resources.qrc
    ```

5.  **Run labelImg:**

    ```bash
    python labelImg.py
    ```

## Project Structure
```
Tensorflow/
├── labelImg/             # Annotation tool
│   ├── data/
│   ├── libs/
│   ├── resources/
│   └── ...
├── scripts/              # Project-specific scripts
└── workspace/            # Project workspace
├── annotations/      # Annotation files      
├── images/           # Image datasets
│   ├── CollectedImages/
│   ├── test/
│   └── train/
├── models/           # Trained models
└── pre-trained-models/ # Pre-trained models
└── ssd_mobilenet_v2_fpnlite_320x320_coco17_tpu-8/
├── checkpoint/
└── saved_model/
└── variables/
collectimg.ipynb      # Scripts for image collection
Tutorial.ipynb        #Script for training data
```
## Usage
1.  **Annotate Images:**

    * Use `labelImg` to annotate the images, creating bounding boxes around the signs.

2.  **Train the Model:**

    * Follow the instructions in the `scripts` directory to train your object detection model.

3.  **Real-Time Detection:**

    * Implement real-time detection and translation using the trained model.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues to suggest improvements or report bugs.
