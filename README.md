# Computer-Vision-Image-classification-assignment
Cats & dogs image classification
![dog or cat](https://github.com/sivanitzhaki/Computer-Vision-Image-classification-assignment/assets/85245749/35d719a6-7d0b-499e-a0c8-30304c623385)

In this project I was given a dataset containing images of cats and dogs. My goal is to classify them correctly. The purpose of this assignment was to experiment with convolutional networks as well as the transfer learning technique. More info down below.

## Data

The dataset has 3200 samples of cats and dogs images of size 180X180 pixels. The data is quite ready for work, so no pre-processing is required and I just split the data into a training, validation and test datasets.

## The model

I examined two CNN models and 1 model using transfer learning: I started by building a four-2d convolutional layers followed by two fully connected layer network. And then I continued with a similar network but with regularization between each layer. Finaly I used transfer learning with ResNet50V2 for it's fast training time and it's high accuracy rate.

I used a fully connected 1D CNN model with an embedding layer and a dropout between the layers. In the FC layers I used the Relu activation function and in the last layer I used the sigmoid activation function for the classification.

| Model | number of epochs | batch size | Loss function | Optimizer | evaluation metric |
|   :---:      |     :---:      |    :---:      |     :---:      |    :---:      |     :---:      |  
| 1   | 	12     | 	32   | binary_crossentropy  | adam    | Accuracy    |
| 2     | 11       | 20     | binary_crossentropy   | adam     | Accuracy     |
| 3     | 10       | 	32      | binary_crossentropy    | adam       | Accuracy     |

## Results

| Model  | Test score (Accuracy) |
| ------------- | ------------- |
| 1  | 0.71625  |
| 2  | 0.75625  |
| 3  | 0.97 |

As expected, the transfer learning model got the best result.
