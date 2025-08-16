# CV_Internship_Tasks_ARCHTECHNOLOGIES
This repository contains implementations of two computer vision tasks completed as part of an internship at ARCH TECHNOLOGIES, Face Mask Detection and Traffic Signs Recognition.

## Task 1: Face Mask Detection

In this task, the goal was to develop a model capable of detecting whether a person is wearing a face mask or not. The dataset originally contained images with face annotations in XML format. These annotations were converted into YOLO text format, which includes normalized bounding box coordinates compatible with YOLOv11. A data.yaml file was created to define the paths for training, validation, and test sets, along with the class labels: with_mask, mask_weared_incorrect, and without_mask. 

YOLOv11 was selected as the detection model due to its efficiency and accuracy in detecting small objects like faces. The model was trained on the prepared dataset, with the training split used for learning and the validation split for monitoring performance. After training, the model was evaluated on a separate test set to measure accuracy and performance.

The trained model can perform inference on both images and videos, drawing bounding boxes with class labels around detected faces. Real-time detection is also supported, and output results can be saved as images or combined videos. This workflow — from XML-to-YOLO conversion, through YOLOv11 training, to evaluation and inference — ensures accurate face mask detection and makes it easy to deploy on image or video data.


## Task 2: Traffic Sign Classification
This task focused on recognizing traffic signs using the German Traffic Sign Recognition Benchmark (GTSRB) dataset. Two different models were implemented and compared:

Custom CNN: built from scratch with convolutional, pooling, and fully connected layers.

MobileNetV2: used pre-trained ImageNet weights with a fine-tuned classifier head.

Data preprocessing involved resizing images, normalizing pixel values, and one-hot encoding labels. Both models were trained and evaluated on the same training-validation split. The Custom CNN achieved a test accuracy of 98%, outperforming MobileNetV2, which achieved 94%. The confusion matrix and classification report provide detailed performance metrics for each class, indicating that the Custom CNN was better suited for this dataset due to its architecture being optimized for traffic sign characteristics.
