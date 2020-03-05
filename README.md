Transfer Learning

this is model tested on dogs breed dataset (http://vision.stanford.edu/aditya86/ImageNetDogs/)

While EfficientNet reduces the number of parameters, training of convolutional networks is still a time-consuming task. To further reduce the training time, we are able to utilize transfer learning techniques.

Transfer learning means we use a pretrained model and fine tune the model on new data. In image classification we can think of dividing the model into two parts. One part of the model is responsible for extracting the key features from images, like edges etc. and one part is using these features for the actual classification. Usually a CNN is built of stacked convolutional blocks reducing the image size while increasing the number of learnable features (filters) and in the end everything is put together into a fully connected layer, which does the classification. The idea of transfer learning is to make the first part transferable, so that it can be used for different tasks by replacing only the fully connected layer (often called “top”).


if you get the OOM error remove the layers
    x = Dense(1024, activation="relu")(x)
    x = BatchNormalization()(x)
   from effn7() function.
