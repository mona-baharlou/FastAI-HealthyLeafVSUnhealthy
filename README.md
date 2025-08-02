## Healthy Leaf vs. Diseased Leaf Classifier
This repository contains an image classification model built to identify whether a plant leaf is healthy or diseased. Using the powerful fastai deep learning library, this project demonstrates a practical application of computer vision, from gathering and preparing data to training a robust model capable of assisting with plant health diagnosis.

This project is a direct application of the concepts taught in Jeremy Howard's Practical Deep Learning for Coders course. It showcases how to leverage transfer learning to build an effective and useful classifier with a minimal amount of code, tackling a real-world problem with an elegant solution.

# How It Works
 - Data Acquisition: Images of both 'healthy leaves' and 'diseased leaves' are automatically scraped from the web using the duckduckgo_search library.
 - The model is trained on this dataset to learn the visual cues of different plant health states.
 - Data Cleaning: Corrupted or non-relevant images are automatically identified and removed from the dataset to ensure a high-quality training set.
 - Data Preparation: The images are organized into classes and prepared for the model using fastai's DataBlock API. This process includes splitting the data into training and validation sets and resizing images to a consistent size.
 - Model Training: A pre-trained ResNet18 model is used as a foundation. The model's final layers are fine-tuned on the new leaf dataset, a technique known as transfer learning, which significantly speeds up the training process and improves accuracy.
 - Prediction: The final trained model can be used to analyze a new image of a leaf and predict whether it is healthy or diseased, providing a confidence score for the prediction.

# Technologies Used
 - fastai: The deep learning library used for training the model.
 - duckduckgo_search: For automated image data collection.
 - pathlib: For managing file system paths.
 - Pillow (PIL): For image manipulation and display.

# Example Output
After training, the model can provide a prediction on a new leaf image:

> This leaf is: diseased leaf.
> Probability it's a healthy leaf: 0.0123
> Probability it's a diseased leaf: 0.9877

![](https://github.com/mona-baharlou/FastAI-HealthyLeafVSUnhealthy/blob/main/HLeaf_DLeaf.png)
