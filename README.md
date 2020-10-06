# GENERATE CAPTION FOR A GIVEN IMAGE

Building a model that can generate description or caption related to the input image using VGG16 network as a feature extractor that extracts features from the image and LSTM model to generate captions. 

The model is trained on Flickr dataset which can be found here https://www.kaggle.com/shweta2407/flickr8k-imageswithcaptions

All the notebooks in this repo shows how to make a deep learning Model for generating caption for any given image. The model will have three parts:

**Image Feature Extractor** - 16 layer VGG model which is pretrained on ImageNet dataset. We will remove the outer 2 dense layer from the architecture and will use the feature extractor part of VGG to preprocess our image dataset.

**Caption Processor** - This model will have one embedding layer with LSTM to process our captions text.

**Image_Caption_Combination** - We will prepare the input dictionary to feed to the final model by mapping the image and text.

**Final Model** - This is the final model in which we input the image features extracted by the "Image Feature Extractor" and text features extracted by the "Caption Processor" and train it to generate captions for any given image.
