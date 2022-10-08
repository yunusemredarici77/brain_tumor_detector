Binary Image classification is one of important topic recently in order to describe pictures as let say real and fake or wearing mask or not wearing mask. Also there are many projects over the medical area currently that are not totally integrated but we can tell brain tumor detection can be also integrated to this field even if there are much improvement.Machines need a lot of training for feature extraction which becomes a challenge due to high computation cost, memory requirement, and processing power.
Nowadays, many new applications of image classification has been tried to decrease the memory requirement, computation cost and increase the accuracy of the classification of images.
Currently those improvent with state of art method reach like VGG21 and denseNet to 97 percent accuracy.
So i discover that we can even increase accuracy by using monte carlo dropout technic. In order to show it i worked on denseNet and custom architectures then i applied MonteCarlo Dropout technic.
DENSENET
DenseNet architecture is  basically layer connections to each other . In this way information from first layer is also direction pass to the last layer.
For L layers, there are L(L+1)/2 direct connections. For each layer, the feature maps of all the preceding layers are used as inputs, and its own feature maps are used as input for each subsequent layers. Since I have used transfer learning over denseNet in order to make the program learn better i have added 5 more trainable layers so with this diffirent dataset model got better accuracy.
/n
Custom Arcitecture
I have used 6 convolution layers with start 16 feature maps and end with 256 feature maps and also each layer are followed by mac pooling and relu activation function. Then fully connected layer has started with 512 nodes by followed relu activation function again.Eventually it ends with output layer with sigmoid function with 1 node.
<img width="271" alt="Picture1" src="https://user-images.githubusercontent.com/56913028/194730932-6511e5a2-66fa-46cf-9e9c-995c2db485ef.png">
DATASET
MRI  dataset (classified as Benign Tumor, Malignant Tumor, Pituitary Tumor, etc. Kaggle )
Subset of the Tiny Images dataset and consists of 7000 160x160x1 color images
Training set consist of 5025 images and Validation set is also consist of 1304. Lastly Test dataset consist of 640 images.
image comes with a ”tumor” label (the class to which it belongs) and a ”no_tumor”
Each ![Picture11](https://user-images.githubusercontent.com/56913028/194730966-088265d5-e0b7-4230-b7b8-1661c684a3e4.gif)
The training set has been split into train and validation. Therefore, the classifier has been trained only on training set, hyper-parameterßs selected based on validation set and the unseen test set has been used to evaluate the model.

MC DROPOUT
Main purpose of this project is to show how effective is MC dropout with architecture. 
We simply apply dropout at test time, Then, instead of one prediction, we get many. We can then average them or analyze their distributions. And the best part: it does not require any changes in the model’s architecture. 
<img width="612" alt="Pictulre1" src="https://user-images.githubusercontent.com/56913028/194730959-f967095d-9dab-40a5-b322-81db9a75da60.png">



