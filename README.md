# Image-captioning
Image captioning using TensorFlow and Flickr30K dataset
In this project I didn't use any pretrained models. Both CNN and LSTM(RNN) models were built with TensorFlow (and Keras) libraries and trained on Flickr30K dataset. Code includes loading the dataset to Google Colab notebook from Kaggle datsets.

General code architecture: flickr30k dataset as input -> cnn model for features extraction -> caption prediction model (RNN LSTM?)

Model architecture illustration:
![image](https://user-images.githubusercontent.com/101993270/230741191-f670f7f2-af54-4643-94b0-4d230011b9fe.png)
