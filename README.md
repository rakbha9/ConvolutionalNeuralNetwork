# Melanoma Detection using custom CNN
> To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
- To build a CNN based model which can accurately detect melanoma and alert the dermatologists about the    
  presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
- The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the  International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken  with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and
  moles, whose images are slightly dominant.

## Technologies Used
- TensorFlow version: 2.18.0
- Keras version: 3.8.0
- Matplotlib version: 3.8.0
- NumPy version: 1.26.4
- Pandas version: 2.1.4
- PIL version: 10.2.0
- Augmentor version: 0.2.12

## Conclusions
- The custom model that has been run without any regularization and augmentation strategy overfits the data.
- We added data augmenationn strategy for the images and then used drop out which improved accuracy and removed  overfitting to some extent. We tried  L1 regularization, but it reduced the accuracy to a greater extent, and  hence went with dropout strategy along with augmentation for images. 
  The model learnt well and is not memorizing training data excessively. The model is improving as training
  progresses since accuracy is increasing and loss is decreasing, but there was some fluctuations in 
  validation loss which might be because of smaller dataset. 
- There was a class imbalance, and lesser images for few categories. Hence we have added 500 images for every
  category, and used the same strategy done above which improved accuracy and reduced loss to a major    
  extent.
- After reblance, training and validation accuracy both increase consistently, except with little variance at
  the end. There is a slight divergence towards later epochs, but validation accuracy is not significantly    lower than training accuracy. Training loss decreases steadily.Validation loss fluctuates slightly but remains close to training loss.
- After rebalancing is better because 
  - More stable validation accuracy (less fluctuation).
  - There is lower validation loss and better alignment with training loss.
  - Better generalization (training and validation accuracy curves are closer).
- Rebalancing helped the model learn more effectively across all classes, reducing bias toward majority    
  classes. This results in better overall model performance and less overfitting.

## Acknowledgements


## Contact
Created by [@rakbha9] - feel free to contact me!
