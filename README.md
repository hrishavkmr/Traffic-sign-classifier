# Traffic-sign-classifier

# Dependencies
1. Python3
2. Keras
3. Tensorflow
4. Pandas
5. Pickle
6. Numpy

To run this code, you can download german traffic signs from the following link:
https://bitbucket.org/jadslim/german-traffic-signs

The German Traffic Sign dataset consists of 43 different traffic sign with each image having 32×32 px size. This dataset has 39,209 images as training data (Using this number of an image we have to train a neural network) and 12,630 images as a test data. Each image is a photo of one of the 43 class of traffic sign.

![Alt text](https://cdn-images-1.medium.com/max/800/1*Ij6RY6VlN-BzccVz__nqgg.png)

While going through each class images and plotting the distribution of a number of images I end up with below graph.

![Alt text](https://cdn-images-1.medium.com/max/800/1*mMigkDLgCsz3oENwoOdUOw.png)
# Augmentation
The dataset we have is fairly unbalanced which might make model more bias towards particular class plus deep learning models may have million of parameters which require vast amount data to tune it. In such cases, image augmentation helps us to generate more and balanced datasets. 

# Model Architecture
I used LeNet as my base model and started playing with it. This is the point where I experimented a lot and tried to tune the parameter in the network (This part took the longest time for this project).

This model is fairly simple and it gave 96% accuracy on test data and 99% accuracy on validation data. 
