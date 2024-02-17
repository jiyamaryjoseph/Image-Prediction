#  Data Science Project: This marks my initial step into image prediction.
Reference : @codebasics


![image](https://github.com/jiyamaryjoseph/Image-Prediction/assets/83010684/6ea792c5-7a24-4d7a-aab8-b9814ba6f088)

# Image Classification Project

This project is my first step into image prediction, inspired by a celebrity face recognition project by @codebasics. It encompasses model building, server development, and user interface (UI) development.

## Introduction

I'm excited to showcase my image classification project, influenced by a celebrity face recognition project. It aided me in recalling all the project components, such as the server, model, and UI. This project marks the beginning of my data science journey, and I'm eager to see where it takes me next.

## Model

### Dataset
The dataset consists of images of my favorite role models:
1. Kalpana Chawla
2. Micheal Obama
3. Nita Ambani
4. Oprah Winfrey
5. Priyanka Chopra

Source: Google Images (webscraping with the help of fatkun-batch).

### Model Building (myrole_model_predic.ipynb)
- The notebook contains the model for predicting the faces of my favorite role models.
- Images are preprocessed by converting to grayscale and detecting faces and eyes using cascade classifiers.
- Images are cropped and saved in a dataset folder.
- Wavelet transformation is applied to images, and raw and wavelet images are combined for training.
- Support Vector Machine (SVM) is used for training with grid searching, achieving 98% accuracy.
- The trained model is saved as a pickle file.

## Server

### server.py
- Flask-based server for running the project.
- Flask provides tools and features for creating web applications in Python.

### utils.py
- Contains common code blocks for classifying images and loading artifacts.

### wavelet.py
- Class for converting raw images into wavelets.

### opencv
- Pretrained models for face and eye detection using Haar cascades.

### artifacts
- Contains pickle file and class dictionary.

## UI

### app.css
- Stylesheet for webpage elements.
- Defines visual presentation of HTML document.

### app.html
- HTML document structure for the webpage.
- Defines the structure and layout of webpage content.

### app.js
- JavaScript code for interactivity and convenience.
- Adds dynamic behavior to HTML elements based on user actions.




                    
                    
                    
                    
                    
                    
              
              
              


       

