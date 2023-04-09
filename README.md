# Image-captioning
Image captioning using TensorFlow and Flickr30K dataset

In this project no pretrained models were used. Both CNN and RNN(LSTM) models were built with TensorFlow (and Keras) libraries and trained on Flickr30K dataset. Code for loading the dataset to Google Colab notebook from Kaggle datasets is included in attached notebook.

## Project description and goals:
The aim of this project is to allow an image features recognition and provide short description of the image based on identified features.
Model, trained on over 30,000 images of Flickr30k dataset, as built with intent to generalize well to any custom user images and photographs. The model is built to identify, recignize and verbaly describe (in short text sentsnce) the objects and main features depicted in the provided image.

Model architecture illustration:

<img src="https://user-images.githubusercontent.com/101993270/230741248-063afd2b-e1d8-4e15-9ad7-fef146a84907.png" width="800" />

Input Dataset: in this project Flickr_30k dataset was used. The dataset containes 31,783 images with corresponding captions (5 versions for each image).

A dataset was devided into Train and Test sets in a ratio of 0.85/0.15 of the existing data. Validation set of 10 images was reserved to illustrate model performance on unseen images. Train set was used to train the RNN model for caption prediction, while the evaluation of model performance made on the Test set. 

Features generated with custom CNN model were saved to .pkl file. Link to that file https://drive.google.com/file/d/1GdVluZCaOIfyZ0zMUeQd7r27nO3APyLm/view?usp=share_link

Caption prediction model having image features and captions from Flickr_30k dataset for a respected images can be found here - https://drive.google.com/file/d/1zcxZ_WcDRwgMaHPnzW0vYknBvv9V3OSm/view?usp=share_link
Both models can be uploaded directly to notebook (google colab). uploading code is included in cells below respective model generation and saving code cells.

Caption prediction model trained using categorical_crossentropy loss function. Loss values are shown below
<img src="https://user-images.githubusercontent.com/101993270/230743078-dafd45b2-6da9-4337-82d2-0ab86f83feb3.png" width="550" />


Model evaluation - correspondance of the predicted captions to the existing dataset captions - were calculated by BLEU scores (1-gram and 2-gram) from Python NLTK library.

<img src="https://user-images.githubusercontent.com/101993270/230744030-f2edab1b-bb93-4ca7-9f90-f9087759a4ba.png" width="350" />

Example of prediction on an unseen image from validation set:
![image](https://user-images.githubusercontent.com/101993270/230742251-0547d956-0fe3-4bb3-bc48-0d100f00dcdf.png)

