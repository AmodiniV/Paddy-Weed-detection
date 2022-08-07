# Paddy-Weed-detection

I. Image Classification:
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

II. Semantic Segmentation:

The goal of this code is to perform site-specific weed management using Semantic Segmentation. 
Annotated images for the semantic segmentation models were generated using playment.io tool. Each RGB original image has a corresponding annotated image with the same name in png format. Each pixel of the annotated image was labeled with a class id: Background—0, Broadleaved weed—1, Sedges—2, Paddy—3. Thus, the entire annotated image has color between 0 and 3.

The Google Colab facility was used for the implementation of this research. Keras, Tensorflow, and image-segmentation-keras APIs were used for the implementation of different models. In the models, transfer learning was used to get better results. Weights obtained from ADE-20 K dataset (Zhou et al., 2017) were used as initial weights in the models. ADE-20 K dataset weights are trained on 150 different classes. Three semantic segmentation models—UNet, PSPNet, and SegNet, were used in this research. These models were implemented with different base models—ResNet-50 and VGG-16. In this research, PSPNet and UNet gave better results with ResNet-50 encoder and SegNet with VGG-16. This code shows the architecture and implementation of PSPNet as it gave the best results.



For further details refer to research paper: https://www.tandfonline.com/doi/full/10.1080/23311916.2021.2018791


