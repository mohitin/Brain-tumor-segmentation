
<img src="https://drive.google.com/uc?id=1GkjZ9W02VQp4w4a4wA70NwRxDcwJJjWd" width="250" height="250" allow="autoplay"></img>


# Automatic Multimodal Brain Tumor Segmentation using Deep Convolutional Neural Networks
## Contributors:
Mohit Kumar Meena (213070021)* \
Harsh Diwakar (213070018)* \
Nihar Mahesh Gupte (213070002)* \
Sunaina Saxena (213070001)* \
** Department of Electrical Engineering -IIT Bombay

This repo contains info for course project of Foundations for Machine Learning (CS 725) at Indian Institute of Technology, Bombay.

# Introduction
Glioma brain tumors are the most common primary brain malignancies, with different degrees of aggressiveness and has variable prognosis. Currently, MRI segmentation of gliomas is largely based on examination of biological tissues in order to observe the appearance of infected cells in microscopic details. Manual tumor segmentation is a tedious, time-intensive task that requires a human expert to delineate components,Therefore manual segmentation often fraught with inaccurate readings and results. So in this project, A fully automated deep learning methods namely, 2D UNet and 3D UNet were implemented to segment out brain tumors into their sub-components. Experimentation of the model were carried out on BraTS 2018 challenge dataset and the results on 2D UNet are found to be more impressive whereas 3D UNet needs more training to perform better which couldn't be done with available dataset. The models are promising to generate good results when applied to independent clincial dataset of both LGG (low-grade glioma) and HGG (High-grade Glioma) patient. Gliomas are further divided into two sub categories namely, HGG (High Grade Gliomas) and LGG (Low Grade Gliomas).

# Dataset and data preprocessing
Datast used in this project is taken from [BraTS 2018](https://paperswithcode.com/dataset/brats-2018-1) challenge. Dataset contains sequences of 210 HGG patients and 75 LGG patients. 
* Each Sequence contains Four different modalities given as T1, T2, T1(Contrast enhanced) and FLAIR(Fluid attenuated inversion recovery).
* Each modalities initially contains sequence with some random dimensiom which is converted into desired format i.e. (X,155,240,240,4)
 * Here, **N**=Number of patients, **155** denotes number of slices,**240*240** is the dimension of each slice and **4** is the number of modalities.
* Each sequence is truncated and each slice is truncated to reduce redundant information.
* For 3D UNet, Tensorflow data pipeline is made to minimize time complexity.


