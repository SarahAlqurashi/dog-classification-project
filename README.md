# dog-classification-project
The dog classification project predicts dog breeds by designing and training a convolutional neural network to analyze images of dogs and correctly identify their breeds for deep learning  Nanodegree program of Udacity. The goal of this project is to predict 133 different dog breeds using 8351 dog images. The algorithm takes an image as an input and if the given image is for humans, the algorithm returns the dog name the most resembles that human. The algorithm trained on GPU.
# Folder Structure:
* The dog_app.ipynb - Jupyter notebook that includes all the code
* The images folder contains sample images
# Datasets: 
The dog_app.ipynb Jupyter notebook include a code that downloads the dataset 
# Porject Steps:
* Human face detection: a helper function that identifies the human face in images using openCvs haarcascades xml. 
* Dog face detection: this step is done using a pre-trained VGG16 model, the dog face detection function output true if a dog image is detected otherwise false.
* Creating CNN from Scratch:  I prepared a CNN architecture from scratch The idea was simple, stacking up 6 convolutional layers after the input layer and adding a max-pooling layer with a 2x2 kernel and stride of 2  in between, After that, I added three fully connected layers for classification. The fully connected takes the feature map from the previous layers after I flatten it to a vector of length 512*3*3 and produce a 133-dim output. To avoid overfitting, I included the first fully connected Dropout layer and I use relu as an activation function.
* Transfer learning using Pre-trained VGG16 CNN: VGG16 has 16 layers with various combinations of convolutional layers. Since the dog data set small, I preserved the wights of the VGG16 model and change the last fully connected layer output from 1000 to 133 to fit the bread classification. The model has with  87% accuracy on the test set.
# Porject Architectures :
* Self made CNN architecture 
* VGG-16 Architecture
# Porject Libraries :
* Pytorch
* OpenCV (Human Face Detection)
* Matplotlib (Plot Images)
* Numpy (Numerical computations)

