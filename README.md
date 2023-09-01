# Wildlife-Image-Processing

![DSC_6383](https://github.com/KimSB80/Wildlife-Image-Processing/assets/124254338/71a00768-6ad9-4374-8873-31c313503559)

## Problem Statement
Camera traps, also known as game cameras, are an important tool for monitoring wildlife populations for conservation and management purposes. The cameras allow for wildlife data to be collected with minimal human disturbance, yielding more accurate data for species presence and interactions. Camera traps produce an enormous number of images, and sifting through these images to identify individual species can be time consuming and tedious. Training machine learning models to identify wildlife in camera trap images can therefore save companies an enormous amount of time and resources. 

## Data Collection
The general focus of this project was to use deep learning to train a convolutional neural network (CNN) model that can accurately predict the animal species in a camera trap image. While camera traps are used for all types of wildlife, monitoring bird populations can be particularly challenging, since they are more difficult to capture and track than other terrestrial animals. For this project, I used a [Kaggle dataset](https://www.kaggle.com/datasets/akash2907/bird-species-classification) containing images of 16 common Himalayan birds.

## Data Wrangling and Exploratory Data Analysis
There was very little meta-data associated with these images, and images were all properly labeled and sorted, so this step was minimal. I examined sample images in each class and determined that there was a large degree of variation in the types of bird photos caught by the camera traps. The pictures vary in the complexity of the background vegetation, the pose/angle of the bird and how obscured it is by vegetation, as well as bird size and how far the bird is from the camera. Some photos also contained multiple birds. Given limited size of the dataset (149 images in the training dataset), this will likely pose challenges, especially for a 16 class image identificaction problem.

Below is a sample of the images for two different species.
<img width="878" alt="Screenshot 2023-08-30 at 3 46 00 PM" src="https://github.com/KimSB80/Wildlife-Image-Processing/assets/124254338/d92881b6-fa64-4126-aacc-14930e30c98c">

## Preprocessing and Modeling
I used the ImageDataGenerator for preprocessing images, which augments the data by randomly shifting, rotating, and flipping the images. I then tried out the following model types and assessed model accuracy and validation loss metric for the following models: <br>

Model 1: CNN model<br>
Model 2: VGG16 pre-trained model<br>

I first used a convolutional neural network (CNN) model for analyzing and classifying bird images into 16 classes. CNN models are a common type of deep learning model used for classifying images. The CNN model model performed very poorly on the validation and test data (even after adding more layers). I then fit pre-trained VGG16 model, which improved training accuracy and validation accuracy by over 30%, but was still prone to overfitting due to the small size of the dataset, and performed poorly on the test data. 

## Summary
This was a good exercise in image classification and CNN models. The main things I learned from this project were:
1. The architecture behind constructing a CNN model, and the increase in model accuracy offered by using a pre-trained model such as VGG16 on image data.
2. The importance of having a large dataset for good results, especially for image classification! While this was an interesting learning exercise, it ultimately did not lead to good modeling results because of the limitations of the dataset, especially for a mulit-class classification problem.
3. Next steps: I am interested in further exploring other pre-trained models such as the ViT transformer model for image data, but on a larger image dataset.

