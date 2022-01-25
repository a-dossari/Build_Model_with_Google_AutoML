# Build a Model with Google AutoML


### **Project Overview**
In this project, we are going to build the classification model that would serve as the backbone of this product. We will use Google AutoML, an automated machine learning tool that will allow us to build the model and host it in the cloud. In order to appreciate how training data impact models, we will build models with 4 variants of the dataset. This project is designed to test your ability to

1. build a model using Google's AutoML Vision platform, and
2. understand how properties of the data impact the performance of models.

### **The Data**
We'll be using [Kaggle chest x-ray dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia), which is the same dataset that we used in the previous project, except here, we'll use the original labels supplied with the data on Kaggle.

### **The Four Parts of the Project**
We will train four different models using four variants of the pneumonia dataset. Recall that the dataset contains childrens' chest x-ray images and that they are classified into two classes, **normal** and **pneumonia**. The following sections describe the steps you must take to create each model.

1. Create a binary classifier to detect pneumonia using chest x-rays
We'll start by training a model simply **using 100 images from the “normal” class and 100 images from the “pneumonia” class**.

2. Create an unbalanced binary classifier
Next, **use 100 images from the “normal” class, and add 200 more "pneumonia" class images**. 

At this moment, the total count of images must be:

* **normal** class = 100
* **pneumonia** class = 300

The model will be trained on very unbalanced classes; this will show you what happens when the number of images in different classes is very different. 

3. Create a binary classifier with dirty data
In this iteration, **start with the original dataset of 100 "normal" and 100 "pneumonia" images**. Then **switch the labels of 30 images in each class**. After you've done this, 30% of the data is mislabeled.

4. Create a three-class model with the classes **normal**, **bacterial pneumonia**, and **viral pneumonia**
For the final model, note that the **pneumonia** images actually have two different classes: *bacterial pneumonia** and **viral pneumonia**. These labels are indicated in the **image filenames**. 

For this model, **add 100 "normal" images, 100 "bacterial pneumonia" images, and 100 "viral pneumonia" images** (for a total of 3 classes). 
