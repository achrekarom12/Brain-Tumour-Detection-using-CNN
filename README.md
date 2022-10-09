# Brain Tumour Detection using Convolutional Neural Networks
Dataset used:  <br><br>
<b>Problem Statement:</b> To detect whether the patient have brain tumour or not from MRI Scans using Image processing and Convolutional Neural Network. <br><br>

<b>Domain:</b> Deep Learning and Computer Vision <br><br>

<b>Methodology:</b> <br><br>

<b>Why Deep Learning?</b><br>
<ul>
<li>When there is lack of clearity about the feature inrospection, Deep learning is used.</li>
<li>Machine Learning models when reached certain threshold limit, don't increase their performance and accuracy. On contrary 
Deep learning models when fed with large number of data produces more accurate results.
</li>
<li>Deep learning works better with huge amount of data. Provided more amount of data it prevents overfitting and also acquires more dimensions.</li>
<li>It can tackle more complex problems like Image Classification, Speech Recognition and Natural Language Processing.</li>
</ul>

<b>What is Deep Learning?</b><br>
<ul>
<li>Imitating structure of human brain.</li>
<li>Deep learning imitates function of human brain to process the data and to create patterns that will help in decision making.</li>
<li>Normally ML models have data and this data is processed in the form of arrays but in DL there's a different concept called 'Tensors' for the same purpose.</li>
<li>In DL when we provide an image, model will learn the different features of that image instead of learning its pixel values.</li>
</ul>

<p align="center">
<img width="415" alt="image" src="https://user-images.githubusercontent.com/88442486/194746232-b0430fab-7595-4415-94f6-404a68b877cb.png">
</p>

<h2>General Intution of Deep Learning:</h2>
<b>Perceptrons:</b> The most basic kind of neural network is a Perceptron. It is a single layer neural network which is used in simple binary classification problem.
Binary classification when given an input which genrally a series of vectors decides whether the given input belong to a certain class or not.
This perceptron is inspired from the real human brain neuron. 
<br> 
<p align="center"> <img width="776" alt="image" src="https://user-images.githubusercontent.com/88442486/194746851-f4fcb0ca-3d37-4dbc-b4ef-be713ec5d72d.png"> </p> <br>
Here x0, x1, x2... are inputs which means these are nothing but input vectors. Thses vectors carries some weight along with them.
w1, w2, w3... denotes weight of that input. Now this weights will decide how much impact will have this input on the final output.
Z is the linear function which is the summation of input vectors, weights and some bias.
To add some non-linearity we have to include a special fuction called activation function. There are several types activation functions.
Some of them are ReLu, Softmax, Tanh etc.
These weights are updated by the taking the loss between actual and expected value of y. <br>
<br> <b>Multilayer Perceptron:</b> <br>
A single neuron is called as a Perceptron. When we combine the multiple perceptrons we have something called as Dense Layer. And when we have many number of layers of these 
many number of perceptrons then we call it as a Multilayer Perceptron. On broader look when we comapre SLP and MLP, SLP is nothing but a Logistic Regression.
Where we can perform for only single class and can not have a look at multiple dimensions. But in MLP we will have multiple dense layers and these dense layers can help us 
to extract multiple features which will eventually result in better accuracy.
Note that a MLP is a subclass of <b>Feedforward ANN.</b>

<h2>Image Processing in Deep Learning:</h2>
<b>Why CNN for Image Processing?</b><br>
<ul>
<li>Suppose I have to detect from an image whether it is a cat or a dog. Suppose I have pass this image to a single neuron neural network. </li>
<li>The image I passsed is suppose 120x120 so my input to the input layer will be one flattened vector of size (1, 120, 120).</li>
<li>This approach can lead to multiple problems:
<ol>
<li>Overfitting of the data</li>
<li>Dimensionalty Curse</li>
<li>Variance in object postion</li>
</ol>
</li>
</ul> 
<br> <p align="center"> <img width="776" alt="image" src="https://user-images.githubusercontent.com/88442486/194752081-78f06e8d-7d3b-4521-b356-0801da095d28.png"> </p><br>
<b>What is CNN?</b>
<ul>
<li>CNN stands for Convolutional Neural Network. It has its major applications in the field of Computer Vision.</li>
<li>It can assign importance to various aspects of the image and is able to differentiate them from one another.</li>
<li>Template matching is the process of moving the template over the entire image and calculating the similarity between the template and the covered window on the image. Template matching is implemente
d through twodimensional convolution.</li>
<li>Components of CNN:
<ol>
<li>Convolutional Filters: Used for feature extraction</li>
<li>Pooling layer: In order to reduce dimension and complexity this layer is used. There are various types of pooling layer called as 
global average pool, maxpool, average pool etc. Pooling layers basically reduces the number of parameters and amount of computation performed 
in the network. It acts like a summerizer. In this layer no features are learnt.
</li>
<li>Padding layer: Used to keep the image size as same as previous. As same as Pooling layer no features are learnt in this layer too. It is genrally
refered as number of pixels added to an image when it is being processed by a filter.
</li>
<li>Flattening: Suppose at the end pooling layer has given us a 12 features so we cannot directly pass this to our dense layer.
We will have to make it as a single array before passing it to MLP. Basically we flatten the output of convolutional layers as a single
long feature vector. And this vector is then connected to final classification model which is also known as fully connected layer.
</li>
</ol>
</li>
</ul>
