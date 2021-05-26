# Paddy-Weed-detection
Using image classification to classify paddy and weed.

Dataset :
There are two types of dataset:
1. Only isolated images for classes : grass,broad-leaves,sedges and paddy.
                                      Training set has 1957 images belonging to 4 classes.
                                      Test set has 116 images belonging to 4 classes.
2. Background subtracted and isolated images : grass,broadleaves and sedges
                                      Training set has 2715 images belonging to 3 classes.
                                      Test set has 175 images belonging to 3 classes
                              
These datasets are not public yet.

Img classification is done using VGG-16 and resnet-50.
Transfer learning is used in both models using ImageNet dataset.

Used Dropout for regularisation to make sure overfitting doesn’t happen. Dropout rate of 0.7 is used
For hyper parameter tuning : tried different learning rates,batch_size,optimisers and dropout rates. 
Finally we are using SGD optimiser with learning rate 0.001 and momentum  of 0.9 


