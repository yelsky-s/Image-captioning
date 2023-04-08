# Image-captioning
Image captioning using TensorFlow and Flickr30K dataset
In this project I didn't use any pretrained models. Both CNN and LSTM(RNN) models were built with TensorFlow (and Keras) libraries and trained on Flickr30K dataset. Code includes loading the dataset to Google Colab notebook from Kaggle datsets.

Model architecture illustration:

<img src="https://user-images.githubusercontent.com/101993270/230741248-063afd2b-e1d8-4e15-9ad7-fef146a84907.png" width="800" />

Input Dataset: in this project Flickr_30k dataset was used. The dataset containes 31,783 images with corresponding captions (5 versions for each image).

A dataset was devided into Train and Test sets in a ratio of 0.85/0.15 of the existing data. Validation set of 10 images was reserved to illustrate model performance on unseen images. Train set was used to train the RNN model for caption prediction, while the evaluation of model performance made on the Test set. 

Caption prediction model trained using categorical_crossentropy loss function. Loss values are showen below
<img src="https://user-images.githubusercontent.com/101993270/230743078-dafd45b2-6da9-4337-82d2-0ab86f83feb3.png" width="550" />


Model evaluation - correspondance of the predicted captions to the existing dataset captions - were calculated by BLEU scores (1-gram and 2-gram) from Python NLTK library.

<img src="https://user-images.githubusercontent.com/101993270/230742050-660345c6-e8f2-4a47-84e2-732d2dcd51f6.png" width="350" />

Example of prediction on an unseen image from validation set:
![image](https://user-images.githubusercontent.com/101993270/230742251-0547d956-0fe3-4bb3-bc48-0d100f00dcdf.png)

