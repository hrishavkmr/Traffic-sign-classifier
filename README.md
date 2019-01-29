# Traffic-sign-classifier

# Dependencies
1. Python3
2. Keras
3. Tensorflow
4. Pandas

To run this code, you can download german traffic signs from the following link:
https://bitbucket.org/jadslim/german-traffic-signs

The German Traffic Sign dataset consists of 43 different traffic sign with each image having 32×32 px size. This dataset has 39,209 images as training data (Using this number of an image we have to train a neural network) and 12,630 images as a test data. Each image is a photo of one of the 43 class of traffic sign.

![Alt text](https://cdn-images-1.medium.com/max/800/1*Ij6RY6VlN-BzccVz__nqgg.png)

While going through each class images and plotting the distribution of a number of images I end up with below graph.

![Alt text](data:image/png;base64,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%0ARU5ErkJggg==%0A)

# Augmentation
The dataset we have is fairly unbalanced which might make model more bias towards particular class plus deep learning models may have million of parameters which require vast amount data to tune it. In such cases, image augmentation helps us to generate more and balanced datasets. 

# Model Architecture
I used LeNet as my base model and started playing with it. This is the point where I experimented a lot and tried to tune the parameter in the network (This part took the longest time for this project).

This model is fairly simple and it gave 96% accuracy on test data and 99% accuracy on validation data. 
