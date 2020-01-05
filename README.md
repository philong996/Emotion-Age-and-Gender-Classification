# Face Detection - Facial Expression+Age+Gender Classification

### Library
`tensorflow 2.0.0`
`opencv`

### Data
The age+gender model is trained on Baidu dataset [link here](https://github.com/JingchunCheng/All-Age-Faces-Dataset)

The facial expression model is trained on Kaggle dataset [FER2013](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data)

### Model
- For **Facial Expression** model, we use 4 convolutional layers with ReLU activation and padding 'same' . See `Fer2013.ipynb` notebook for more details about the model.

![](https://i.imgur.com/skdNLG4.png)



### Training
#### Facial Expression training
- The data from the Kaggle dataset is already split into train and test set. The data is processed from csv file into numpy arrays and fetched into ImageDataGenerator. See jupyter notebook `FER2013.ipynb` for more details.

- Our model achieved ~96% accuracy on train set and ~60% on validation set after 25 epochs (batch size 32)
#### Age and Gender training
* The dataset for age and gender prediction is taken from Baidu's All-Age-Faces (AAF). The dataset contains 13322 face images (mostly Asian) distributed across all ages (from 2 to 80), including 7381 females and 5941 males.

### Flask app
-  Our Flask app connects to the webcam which user can use to scan their faces for classification, which will output the user's age, gender and emotion. 
