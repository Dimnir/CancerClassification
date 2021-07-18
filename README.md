## Colorectal Cancer Classification

__Projects Goal:__ Classification of colorectal cancer histology. <br />

__Environment:__ Jupyter Notebook, Google Colab, Python <br />


### General info:
Building a model which classifies human colorectal cancer tissues into 8 different classes. <br />

#### Datasets:

1) `colorectal_histology` - 5,000 150x150 images of human tissues with different textures from 8 classes with labels.
2) `colorectal_histology_large` - 10 5000x5000 images of human tissues without labels.

#### Main Steps:

First Dataset:

1) seperating images from the first dataset into 90% train and 10% test

2) using a VGG16 model with a custom classifier on top to fit images from first dataset. 

3) freezing first layers of the VGG16 and training the classifier on the images. 

4) data augmentation, unfreezing and fine tune to get better results.

Second Dataset:

5) cropping the large (5,000x5,000) images into 150x150 windows to make it fit the models input

6) predicting the class of each cropped window and combining the windows back to 5000x5000 image for each image from second dataset


#### Results:

Final result:
- multi-class visualization when each predicted class gets its own color
- heatmap of the probability of cancer (1 - high probability , 0 - low probability)

---
![results image](/images/RESULTS.png)
---

more info and code can be found in the notebook - [`CancerClassification.ipynb`](/CancerClassification.ipynb)
