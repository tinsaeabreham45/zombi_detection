# Zombie Detection Project

This project is a computer vision project that aims to detect zombies in images and videos. It was developed as part of the DeepLearning.AI Advanced Computer Vision Specialization.

## Project Description

The project utilizes object detection techniques, specifically the TensorFlow Object Detection API, to identify and locate zombies in visual data. The project includes the following key steps:

* **Setting up the Environment**: Cloning the TensorFlow models repository and installing the necessary dependencies.
* **Data Preparation**: Downloading and preprocessing the zombie detection dataset.
* **Model Training**: Training an object detection model (e.g., Faster R-CNN, SSD) on the prepared dataset.
* **Inference**: Using the trained model to detect zombies in new images and videos.
* **Visualization**: Visualizing the detection results by drawing bounding boxes around detected zombies.

## Demo

Here's a demo of the zombie detection in action:

![Zombie Detection Demo](zombie-anim (1).gif)

## Installation and Setup

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Mount Google Drive (if using Google Colab):**

    ```python
    from google.colab import drive
    drive.mount('/content/drive')
    ```

3.  **Navigate to the project directory:**

    ```bash
    %cd /content/drive/MyDrive/Colab_Notebooks/Advanced_CV/zombi_detect
    ```

4.  **Clone the TensorFlow models repository:**

    ```bash
    !rm -rf ./models/
    !git clone --depth 1 [https://github.com/tensorflow/models/](https://github.com/tensorflow/models/)
    ```

5.  **Pin the TensorFlow models version:**

    ```bash
    !sed -i 's/tf-models-official>=2.5.1/tf-models-official==2.15.0/g' ./models/research/object_detection/packages/tf2/setup.py
    ```

6.  **Install the Object Detection API:**

    ```bash
    !cd models/research/ && protoc object_detection/protos/*.proto --python_out=. && cp object_detection/packages/tf2/setup.py . && python -m pip install .
    ```

## Usage

1.  **Prepare your dataset:** The notebook assumes you have a dataset of images and annotations. Modify the notebook to point to your data. The expected format is likely Pascal VOC or COCO.

2.  **Configure the model:** Choose an object detection model (e.g., Faster R-CNN, SSD) and configure its parameters in the configuration file. You'll need to update the configuration file path.

3.  **Train the model:** Run the training script, providing the path to the configuration file and the training data directory.

4.  **Run inference:** Use the trained model to detect zombies in images or videos. The notebook contains code for this.

## Code Description

* `Untitled0 (1).ipynb`: This Jupyter Notebook contains the complete code for the zombie detection project. It includes the steps for data preparation, model training, inference, and visualization.

## Results

The notebook includes code to generate a GIF animation of the zombie detection results. The animation shows bounding boxes around detected zombies in a video.

## Dependencies

The project relies on the following main libraries:

* TensorFlow
* TensorFlow Object Detection API
* OpenCV
* Matplotlib
* imageio
* Other libraries specified in the `setup.py` file within the TensorFlow Object Detection API.

## Notes

* This project was developed using Google Colab, but it can be adapted to other environments with some modifications.
* The project uses a specific version of the TensorFlow models repository (2.15.0) for compatibility.
* The training process can be computationally intensive and may require a GPU.
* The paths to the dataset, configuration files, and model checkpoints may need to be adjusted based on your local setup.

## Author

Your Name

## Acknowledgements

* DeepLearning.AI for providing the project as part of the Advanced Computer Vision Specialization.
* TensorFlow for the Object Detection API.
