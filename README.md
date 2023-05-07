# Breast-Cancer-Detector
The CNN model is used for training the data very often in medical image diagnosis, analysis
and its applications. In fact, the medical imaging in CAD system becomes successful because
of CNN use [28, 29]. This substantiates the use of CNN for our application in breast cancer
detection, of course with some improvement or enhancement. Generally, a CNN comprises of
hundreds of neurons structured in different layers, forming the kernels. The size of kernels is
chosen small as the depth of input image has to be same. A receptive field which is actually a
small region, is connected with neurons. This is done because it is very difficult to connect all
neurons to the previous outputs, especially when the input has high dimensional images. Let
us understand by an example: For an image of size 100 x 100 having 10000 pixels, there are 100
neurons which will require or produce 1000000 parameters. Now, each neuron does not need
to have weight of full input dimension, rather the neuron will hold the weight corresponding
to the kernel dimension since the kernels of small dimension have been connected with neurons.
The kernel needs to slide over the image both in height and width so that high level features
are extracted and two-dimensional (2D) activation map is produced. The rate of sliding
can also be controlled using a suitable parameter. Finally, the output of convolution layer is
stacked and activation map defines the input for next layer to be propagated.
Our architecture is based on the Sequential model, which allows the model to stack sequential
layers of the network in order from input to output. The convolution layer uses filters that
perform convolution operations as it is scanning the input image with respect to its dimensions.
Its hyper-parameters include the filter size and stride, which represents the step size
between consecutive receptive filters. The resulting output is called feature map or activation
map. First 2D convolutional layer is added to process the input breast images. The first argument
passed to the convolution layer function is the number of output channels and in our
case, we have used 16 output channels. In our model, we have used 3x3 filter kernel, with stride
1, which slide across the width and height of the image, to perform spatial convolution. During
the experiments we have also experience with different kernel size (from 1 to 7) to analyze the
differences. We have noticed that the small kernel size 1×1 acts as a bottleneck. We have considered
padding so that the input image gets fully covered by the filter and stride specified in
this model. We have applied the rectified linear unit (RELU) activation function
