# Project Name
> This project is aimed at building a Custom CNN model to accurately detect skin cancer called melanoma from images. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Use the image files available to classify them into various category of skin cancers
- What is the background of your project? Skin Cancer detection
- What is the business probem that your project is trying to solve? Early detection of skin cancer called Melanoma from skin images
- What is the dataset that is being used? The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant. Of the 2357 images, 2239 images were kept for training and 118 was used for validation.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- A normal CNN network was used initially with 3 Conv2D layers using 16,32 and 64 filters of size ((3,3). With 20 epochs, the model accuracy was 87.9% with loss as 0.3123. But the validation accuracy dropped significantly to 50.7%. This clearly indicated that there was need to incorporate techniques like data augmentation, dropout to control overfit.
- In the second round of custom CNN model training, 2 new features were introduced. One was to do RandomFlip, RandomRotation and RandomZoom on the input images. Second was to introduce a dropout layer after the CNN layers. These 2 changes helped to narrow down the difference between the training accuracy(62%) and validation accuracy(57.27%). However there are still few things to take care which could improve accuracy.
- In the third round of training, we looked at the distribution of images available for the 9 classes of diseases. It was found that there was under 100 images for classes like dermatofibroma while over 400 images was present for classes like melanoma, pigmented benign keratosis. Hence in order to tackle the class imbalance, a python library called Augmentor was used for artificial generation of image data. These added around 500 images to each class. 
- The final CNN training therefore had around 5392 images for training and 1347 images for validation. An additional layer to normalize the output was introduced called Batch Normalization. With this network, the accuracy for both the training and validation stood at 77%. 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- TensorFlow - version 2.18.0
- Keras - version 3.8.0
- Augmentor - version 0.2.12

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by Upgrad course.

## Contact
Created by [@AnuThomas2000] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
