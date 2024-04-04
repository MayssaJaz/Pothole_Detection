# Pothole_Detection
## Project Purpose
The objective of this project is to conduct experimentation using the computer vision model **YOLO** (You Only Mook Once), with the aim of assessing its efficiency in the detection of potholes within roadways. 
## Dataset
Our dataset consists of 618 annotated instances of images featuring potholes. These annotations were meticulously crafted using the online CVAT annotation tool, with bounding boxes employed to precisely delineate the pothole areas within the images. The following is an example of an annotated image:

## Explanation
Our training procedure was conducted using the notebook `notebook/pothole_detection.ipynb`. The objective was to fine-tune the YOLOv8 model with our annotated dataset, enhancing its capability to detect potholes effectively. For this purpose, we created our dataset in the structure and format that is supported by the YOLO model:
```bash
    dataset/
    ├── train/
    │    ├── images
    │    └── labels
    │
    ├── test/
    │    ├── images
    │    └── labels
    │
    ├── valid/
         ├── images
         └── labels
```
### Evaluation
The following graph illustrates the incremental enhancement in model performance detecting potholes across epochs. As we can see, the bounding-box loss (**box_loss**) which measures how tight the predicted bounding box is compared to the ground truth is imroving smoothly over each epoch. Additionally, the cross-entropy (cls_loss), which measures the accuracy of classifying objects as potholes ( with a binary classification problem: **pothole** and **background**), notably improves as well.
### Inference
The following images provide illustrative instances of object detection achieved using of the fine-tuned version of YOLO on our dataset.





