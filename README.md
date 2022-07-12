# Surface-Crack-Detection-using-Open-CV
Problem Definition
Surface cracks in concrete structures are an important indicator of structural safety and deterioration. Human surface examination takes time and can yield inconsistent results due to the inspectors' differing empirical knowledge. As a result, a strategy based on computer vision and a CNN model has been proposed for accurately detecting the rich concealed views.

Objectives
To reduce the surface examination time and yield consistent results.
To accurately detect the hidden sights on the surface.
Building a continuous autonomous system to inspect the structures, buildings, monuments to prevent accidents.

Dataset Description and Data Pre-processing
The dataset contains images of various concrete surfaces with and without crack. The image data are divided into two as negative (without crack) and positive (with crack) in a separate folder for image classification. Each class has 10000 images with a total of 20000 images with 227 x 227 pixels with RGB channels. This dataset is taken from the website Mendeley Data - Crack Detection, contributed by Çağlar Fırat Özgenel.

Before creating and training the CNN architecture model, image pre-processing is undertaken. Surface quality and lighting conditions vary widely among high-resolution pictures. There was no data augmentation in terms of random rotation or flipping. Data normalization is to reduce the pixel values in range 0 to 1 so that the pixel numbers are small and are easier and faster for the computation process. As a result, dividing all of the numbers by 255 converts them to a 0 to 1 range.

Tasks performed 
Load Dataset
Using cv2 library to read and load the images. Resizing the images is also done.
Visualizing the Dataset
Visualizing the images and dataset using matplotlib.pyplot.
Normalizing image data
Normalizing i.e reducing the values of pixels in the range 0 to 1 for faster computation.

CNN is a type of algorithm that consists of an input, an output, and many hidden layers. The hidden layer includes convolution layer, pooling layer, rectified linear unit layer (ReLu). Dropout is being used to reduce the overfitting problems. Sequential() model is been used to build the cnn model
Model Training-
Accuracy can be increased by increasing the number of epochs. Learning rate is also important here. Better results can be achieved by training at different learning rates. The best learning rate can be found by trying. Or grid search method can be used. But this increases the training time considerably. Loss = binary_crossentropy, optimizer = adam, epochs = 3, batch_size = 64 etc hyperparameters have been used.
Classification Report-
The classification_report function builds a text report showing the main classification metrics. Precision for each class, it is defined as the ratio of true positives to the sum of true and false positives. Recall for each class, it is defined as the ratio of true positives to the sum of true positives and false negatives. F1 scores are lower than accuracy measures as they embed precision and recall into their computation.
Result-
As a result, 99% success has been achieved. The accuracy and loss function can change by changing the learning rates or changing the number of epochs.





