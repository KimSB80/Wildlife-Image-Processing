# Wildlife-Image-Processing

![DSC_6383](https://github.com/KimSB80/Wildlife-Image-Processing/assets/124254338/71a00768-6ad9-4374-8873-31c313503559)

## Problem Statement
Camera traps, also known as game cameras, are an important tool for monitoring wildlife populations for conservation and management purposes. The cameras allow for wildlife data to be collected with minimal human disturbance, yielding more accurate data for species presence and interactions. Camera traps produce an enormous number of images, and sifting through these images to identify individual species can be time consuming and tedious. Training machine learning models to identify wildlife in camera trap images can therefore save companies an enormous amount of time and resources. 

## Data Collection
The general focus of this project was to use deep learning to train a convolutional neural network (CNN) model that can accurately predict the animal species in a camera trap image. While camera traps are used for all types of wildlife, monitoring bird populations can be particularly challenging, since they are more difficult to capture and track than other terrestrial animals. For this project, I used a [Kaggle dataset](https://www.kaggle.com/datasets/akash2907/bird-species-classification) containing images of 16 common Himalayan birds.

## Data Wrangling and Exploratory Data Analysis
There was very little meta-data associated with these images, and images were all properly labeled and sorted, so this step was minimal. I examined sample images in each class and determined that there was a large degree of variation in the types of bird photos caught by the camera traps. The pictures vary in the complexity of the background vegetation, the pose/angle of the bird and how obscured it is by vegetation, as well as bird size and how far the bird is from the camera. Some photos also contained multiple birds. Given limited size of the dataset (149 images in the training dataset), this will likely pose challenges, especially for a 16 class image identifaction problem.

Below is a sample of the images for two different species.
<img width="878" alt="Screenshot 2023-08-30 at 3 46 00 PM" src="https://github.com/KimSB80/Wildlife-Image-Processing/assets/124254338/d92881b6-fa64-4126-aacc-14930e30c98c">

## Preprocessing and Modeling

