# Convolutional-Neural-Networks-CNN

Implementing Fully Connected and Convolutional Neural Networks(CNN) by Tensorflow and Keras in Python\
Presented to Prof. Majid Ahmadi\
Elhamsadat Hejazi(https://www.linkedin.com/in/elham-hejazi)

## Overall Context

## Introduction 
In this project, I'll create a deep learning model to perform on the MNIST handwritten dataset nearly at the cutting edge. I'll combine Keras and TensorFlow.

### MNIST Dataset
The National Institute of Standards and Technology provided many datasets of scanned documents, which were used to create this dataset (NIST). The size and centering of these pictures were adjusted. Each picture measures 28x28 pixels (784 pixels). An algorithm was trained on 60,000 photos, and then tested on 10,000. A prediction error of 1% is achieved with excellent results. Modern results are around 0.2%, and a large convolutional neural network might attain them.

## Fully Connected Neural Networks
To compare our convolutional neural network, which we will employ later, I begin with a baseline model. We flatten our 28 by 28 pixel photos into a single 784 length vector for each image in order to do a Fully Connected Neural Network. Then, in order to facilitate the functioning of our neural network, I alter the grayscale values from 0-255 to 0-1 (Normalization). We then convert the categories 1 through 9 into a binary matrix. Here is my current neural network model:

Model: "sequential_1"

Layer1:\
Layer (type): dense_1 (Dense), Output shaper: (None, 512), Param: 401920    

Layer2:\
Layer (type): dense_2 (Dense), Output shaper: (None, 512), Param: 262656    

Layer3:\
Layer (type): dense_3 (Dense), Output shaper: (None, 10), Param: 5130   

Total params: 669,706\
Trainable params: 669,706\
Non-trainable params: 0

## Convolutional Neural Networks
I achieved an great 1-2% mistake rate, which was as intended. In this case, I use the Kera library to build convolutional neural networks. Convolutional layers, pooling layers, and FCC layers are just a few examples of how I'll utilise a contemporary CNN implementation. A convolutional layer with 32 feature maps, each measuring 5 by 5, is added. This is also our input layer, and it anticipates the addition of photos. I then specify a 2 x 2 pool size. Finally, we produce probability-like predictions for each prediction class using 10 neurons with a softmax activation function. Here is my current neural network model:

Model: "sequential_3"\
conv2d_1 (Conv2D)            (None, 28, 28, 32)        832\       
max_pooling2d_1 (MaxPooling2 (None, 14, 14, 32)        0 \        
conv2d_2 (Conv2D)            (None, 14, 14, 64)        51264 \    
max_pooling2d_2 (MaxPooling2 (None, 7, 7, 64)          0     \    
flatten_1 (Flatten)          (None, 3136)              0        \ 
dense_5 (Dense)              (None, 1024)              3212288  \ 
dense_6 (Dense)              (None, 10)                10250  \

Total params: 3,274,634\
Trainable params: 3,274,634\
Non-trainable params: 0



