# Traffic-Sign-Classification
In this project, classification of traffic sign is done using machine learning. A large dataset of images was taken as the input and a model is generated which gave us a maximum of 96% of accuracy score.

Our ‘train’ folder consists of 43 folders which all represents different classes by themselves. The range of the folder is 0 to 42. We iterate over all the classes and append images and their respective labels in the data and labels list with the help of OS.

The PIL library is used to open image content into an array and we have successfully gathered all the images and labels in the lists.

The data shape is (39209, 30, 30, 3), means that there are 39,209 images of size 30×30 pixels and 3 means the data consists of colored images (R-G-B value).
From the “sklearn” package, we use the “train_test_split()” method to split, train and test data.
From the “keras.utils” package, we use “to_categorical” method to convert the labels present in “y_train” and “t_test” into one-hot encoding.

To classify the images into their respective categories, we will build a CNN model(Convolutional Neural Network). CNN is best for image classification purposes.

We compiled the model with Adam optimizer which performs well and loss is “categorical_crossentropy” because we have multiple classes to categorize.

After building the model architecture, we then tried to train the model using model.fit(). We tried with batch size 32 and 64. Our model performed better with 64 batch size. And after epochs reaches to 25 the accuracy got stabilized.

After that, we havew got an accuracy score of 96% from out model and after saving the model wer have also create a GUI(Guided User Interface) to check if the model is working fine or not. 
