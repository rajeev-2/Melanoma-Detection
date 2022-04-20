# Melanoma Detection

> Melanoma type of Skin cancer detection with different convolutional neural networks. In our solution, we used different base models with the same top layers to detect melanoma images from others images. There are 9 different classes of skin cancer in the assignment.

## Table of contents

* Melanoma Detection
   * General info
   * Directory structure and files
   * Technologies
   * Setup
   * Results
   * Contact
   * References

## General info

Among skin cancer diseases, melanoma is one of the most common and most dangerous ones, being difficult to detect and causing serious problems once spread deeper. Melanomas have many different shapes, sizes, and colours, thus making it harder to provide comprehensive warning signs. Detecting melanoma early is of utmost importance. Neural Networks provide significant progress in this field, making it possible to detect melanomas with many previously learned patterns, dealing with larger datasets than a human specialist can handle.



## Directory structure and files

Images can be downloaded from the below link
https://drive.google.com/file/d/1xLfSQUGDl8ezNNbUkpuHOYvSpTyxVhCs/view

In the assignment, Images uploaded through Google drive
'/content/gdrive'



## Technologies

- Google Colaboratory
- Google Drive
- Keras
- Python



## Setup

1. Dataset is stored in the google drive as shown in the directory structure section.

2. Mount data.

   ```python
   from google.colab import drive
   drive.mount('/content/gdrive')
   ```

3. Path to Train and Test data sets were linked from the gdrive itself
   

## Results
The different models performed as the followings:
* Base model was overfitting with big difference in Training and Validataion dataset accuracies. The validation set accuracy was very low (~52%)
* With some augmentation technique and Dropout laters, the overfitting was somewhat resolved in 2nd model, but the sccuracies of training also went down (~67%) with no improvement in validation set accuracies. Hence case of Underfitting
* Class imbalance was present, as seen in the bar chart and we need to address this issue with further augmentation
* For Final model, Augmentor library was used and 500 Images were added to each class to remove class imbalance. This helped, as both training and Validation accuracies increased significantly. Validation accuracy was ~79% after running the model for 30 epochs


## Contact

* created by Rajeev Ranjan
* https://github.com/rajeev-2/Melanoma-Detection


## References

* Stackoverflow
* Kaggle
* Upgrad course contents
