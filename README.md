##Project Overview:
The model developed in this project takes an image as an input and the following steps are followed:
•	When an image is given, we first use Person Detector module, which will recognize whether the given picture contains a person or not.
•	Simultaneously, the same image is tried on Dog Detector module to test whether the given picture contains a dog.
•	If it is clear that the image is of a person or a dog, then we will use the Dog Breed Classifier module, which can tell us the dog breed that the person/dog belongs to. If it is neither a person or a dog, then we raise an error.

##Project motivation:
The goal of the project is to identify a dog according to his breed. If the image is that of a human, it would recommend the most similar dog breed. I decided to work on this because Image classifier is one of the hot topics in the Machine Learning field I find it quite interesting wanted to dive deeper into this with some practical work.

##Steps Involved:
1.	Importing datasets
2.	Creating a Human face detection module
3.	Creating a Dog detection module
4.	Creating a Convolutional neural network to Classify Dog Breeds (from Scratch)
5.	Using transfer learning to fine-tune a CNN to Classify Dog Breeds.
6.	Writing and testing the overall Algorithm

##Libraries:
1.	Python 3.7+
2.	OpenCV
3.	Scikit-Learn
4.	Matplotlib
5.	glob
6.	NumPy
7.	Keras
8.	tqdm
9.	Tensorflow

##Dataset:
The datasets are provided by Udacity, the details found after loading the data set are mentioned below:
1.	There are 133 total dog categories and 8351 total dog images
2.	Training dog images: 6680
3.	Validation dog images: 835
4.	Test dog images: 836
5.	There are 13233 total human images.

##Files in the repository:
1. dog_app.ipynb: Notebook to process data, train and explore models and perform final evaluation
2. README.md: Readme explaining the overview of the project


##Project Analysis:
Here, a pre-trained ResNet-50 model is used to detect dogs in images along with weights that have been trained on ImageNet which is a very large and popular dataset used for image classification and other vision tasks.

###Creating a CNN to Classify Dog Breeds (from scratch) –
This network was trained for 5 epochs. At 5th epoch, validation accuracy was 0.03. The test set accuracy was 4.4258%.

###Using transfer learning to fine-tune a CNN to Classify Dog Breeds
This network was trained for 50 epochs. At 50th epoch, validation accuracy was 0.5. The test set accuracy was 50.4785%.

 ###Create a CNN to Classify Dog Breeds (using Transfer Learning)
Here, the model we’re choosing makes use of the inceptionv3 model as a feature extractor, with default weights trained on ImageNet for classification. Hence, it is capable of extracting features for the generic task of object recognition.
This model obtains a test accuracy of ~ 80%. We don’t do any hyper paramter tuning, which can improve the accuracy further. By default, we use a batch size of 20 and the default learning rate.

##Conclusion:
The output is much better than what was expected. I was pleasantly surprised about the effectiveness of the InceptionV3 bottleneck features.

##Acknowledgement:
Thanks to Udacity for providing datasets with dog and human images and some template code which has guided me through out this project.
