# Keras-Model-deployment with Flask API

I used the Keras Sequential model API. The Sequential model is a linear stack of layers. The layers of the CNN are:

 a) 2D convolution layer[Conv2D(filters, kernel_size]
 
 filters: Integer, the dimensionality of the output space (i.e. the number of output filters in the convolution).
 
 kernel_size: An integer or tuple/list of 2 integers, specifying the height and width of the 2D convolution window.
 
 I used 8-filters each of the filter has (3,3)convolution. And the input_shape=(1,28,28),grayscale image with size(28,28)
 
 Activation function is "relu"
 
 b)MaxPooling2D(pool_size=(2, 2))
 
 c) Flatten layer: Flattens the input
 
 d) Dense layer:4 layers with an activation of "softmax"
 
 e) output dense layer
 
For loss crossentropy and adam optimizer. Model.fit, I used batch size 32 means at a time only 32 images will load in memory and epoch =3 only
 
Train result:
error is 6.77% validation acuuracy 93.23% after 3-epoch
 
Test(deploy with a flask API)
We can call the API from mobole app.
 
