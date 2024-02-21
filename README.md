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
- 
![image](https://github.com/jiyamaryjoseph/Laptop-Price-Prediction/assets/83010684/c5950a93-7011-486c-a0ad-00541c4b9d60)

# Image Prediction Deployment on AWS EC2



## Step 1: Set up EC2 Instance
- Launch an EC2 instance with Ubuntu OS
- Configure security groups to allow inbound traffic on ports 22 (SSH) and 80 (HTTP)

## Step 2: Install Required Packages
- SSH into the EC2 instance
- Install Python, pip, and required dependencies for the image prediction application

## Step 3: Set up Nginx Reverse Proxy
- Install Nginx on the EC2 instance if not already installed
- Configure Nginx as a reverse proxy to forward HTTP requests to the Flask application running on a specific port (e.g., 5000)

### Configure Nginx
1. Install Nginx if not already installed:
    ```bash
    sudo apt update
    sudo apt install nginx
    ```

2. Create a configuration file for the image prediction application:
    ```bash
    sudo nano /etc/nginx/sites-available/imgpred.conf
    ```

3. Add the following configuration to the `imgpred.conf` file:
    ```nginx
    server {
        listen 80;
        server_name imgpred.com;
        root /home/ubuntu/ImagePrediction/UI/;
        index app.html;
        location /api/ {
            rewrite ^/api(.*) $1 break;
            proxy_pass http://127.0.0.1:5000;
        }
    }
    ```

4. Save and close the file.

5. Create a symbolic link to enable the site:
    ```bash
    sudo ln -s /etc/nginx/sites-available/imgpred.conf /etc/nginx/sites-enabled/
    ```

6. Test the Nginx configuration for syntax errors:
    ```bash
    sudo nginx -t
    ```

7. If the syntax is OK, reload Nginx to apply the changes:
    ```bash
    sudo systemctl reload nginx
    ```

### Verify Configuration
- Verify that Nginx is running and listening on port 80:
    ```bash
    sudo systemctl status nginx
    ```
- Access the domain name or public IP of your EC2 instance in a web browser to confirm that the reverse proxy is correctly forwarding requests to the Flask application.

unlink the default file in etc/nginx/sites-enabled and symlink with ingpred.conf
## Step 4: Deploy Flask Application
- Transfer the Flask application code and the trained model to the EC2 instance using WinSCP
- Run the Flask application using Gunicorn or any other WSGI server

## Step 5: Test the Deployment
- Access the EC2 instance's public IP or domain name in a web browser
- Upload an image to the deployed application and verify the prediction results


                    
                    
                    
                    
                    
                    
              
              
              


       

