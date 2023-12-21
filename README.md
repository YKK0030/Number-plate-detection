For dataset with annotations use this link :- https://www.kaggle.com/datasets/andrewmvd/car-plate-detection


# License Plate Detection

This project detects license plates in images using a custom trained TensorFlow object detection model.

## Overview

- Uses TensorFlow Object Detection API to train a custom SSD model on license plate data
- Model is trained on annotated images of cars with license plates
- Produces bounding boxes around license plates in new images
- Applies OCR on the detected ROI to read the license plate text

## Model Architecture

The model architecture is SSD MobileNet V2 FPNLite pretrained on COCO dataset and fine-tuned on custom license plate data.

## Usage

`number_plate_detection.ipynb` - Main notebook to view demo predictions on test images.

The trained model files are in `/Tensorflow/workspace/models/my_ssd_mobnet`

To use the model on new images:

- Load model pipeline config and build detection model
- Restore checkpoint
- Run inference using detect_fn() on input image
- Filter detections by threshold and apply OCR


## References

- TensorFlow 2 Object Detection API
- Papers/tutorials referred for implementation


