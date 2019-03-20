# VGG19_SVM_model
A Keras implementation of **VGG19-SVM model** to predict malaria from microscopic images

**To view ipynb files go to html directory. The ipynb files are converted into html for easy access in browser itself.**

This implementation is based on a research paper by professors Dr. Rajesh Kanna B, Dr. Vijayalakshmi A., Mr. Dinesh Jackson. The paper is also uploaded in the repo.

**fine_tune_model.ipynb** contains the code to fine tune the VGG19 model which is trained on imagenet dataset for the malaria dataset. The softmax layer is removed and replaced with another softmax layer with two classes. Either 0 or 1. Whether the given microscopic image of blood sample has or doesnt have malaria. This finetuned model 

**extract_features_finetune.ipynb** contains the code to extract feature vector after the fifth convolution block and before the fully connected layer of the above fine tuned model. The feature size is (7x7x512) which on flattening gives feature vector of size (1x25088) for every image (in both test, validation sets ) and is saved to a pickle file for future use.

**svm.ipynb** contains the code to train SVM on the features extracted from the finetuned model. This trained model can be used to predict if a image has malaria or not.

**data.zip** contains the dataset.

Note: - Code is not commented. 
