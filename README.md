## Real Time Object Detection & Classification
<div align="center">
  <img src="https://github.com/HassanKhalil321/GestureVision/blob/main/assets/final_model.jpg" width="1000"/>
</div>


## Introduction
Welcome to GestureVision, a cutting-edge project focused on the detection and classification of sign language gestures using computer vision and machine learning techniques. GestureVision leverages advanced image processing and machine learning models, including fine-tuning and transfer learning, to accurately detect and classify hand gestures used in sign language. This project aims to bridge the communication gap for individuals with hearing impairments by providing a robust and reliable sign language recognition system.

## Dataset 
The **sign-language-sokd** dataset from Hugging Face is used, a specialized dataset designed for sign language recognition. This dataset includes 720 images across 27 classes, with annotated bounding box coordinates in the COCO format.

<H1 align="center">BBOX_MODEL</H1>

*Input*: The model accepts input frames of size 640x640 pixels.

*Base Model*: EfficientNetB0 serves as the foundational architecture for feature extraction, leveraging pre-trained weights from ImageNet to capture hierarchical features relevant to sign language gesture recognition.

*Layers*: Following feature extraction, Global Average Pooling and Dense layers are employed to further process the extracted features, optimizing the representation for subsequent tasks.

*Output*: The model produces precise bounding box coordinates formatted according to the COCO standard, facilitating accurate localization and recognition of sign language gestures within images.

## Loss
<div align="center">
  <img src="https://github.com/HassanKhalil321/GestureVision/blob/main/assets/mae.jpg" alt="Gesture Recognition" width="600"/>
</div>


## Processing Between Models 

After our BBOX_MODEL provides the bounding box coordinates, we will take the image inside the bounding box with some additional area to make the hands easier to classify and to enhance the efficiency of our classification model.

<H1 align="center">CLASSIFICATION_MODEL</H1>

*Input*: The model accepts input frames of size 640x640 pixels.

*Base Model*: EfficientNetB0 serves as the foundational architecture for feature extraction, leveraging pre-trained weights from ImageNet to capture hierarchical features relevant to sign language gesture recognition.

*Layers*: Following feature extraction, Global Average Pooling and Dense layers are employed to further process the extracted features, optimizing the representation for subsequent tasks.

*Output*: The model outputs class probabilities with a softmax activation function, facilitating accurate classification of sign language gestures.
## Loss

<div align="center">
  <img src="https://github.com/HassanKhalil321/GestureVision/blob/main/assets/cce.jpg" width="600"/>
</div>
