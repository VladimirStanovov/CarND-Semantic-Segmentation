# Semantic Segmentation
### Goal
The main goal of this project is to perform semantic segmentation of road images - detect driveable areas with fully convoluional networks - FCNs. The network layers used are pre-trained layers from VGG-16.

### Solution structure

FCN consists of an encoder, 1x1 convolution and a decoder, or transformed convolution. The pre-trained layers are layers 3, 4 and 7 from the VGG-16 network, which are connected with 1x1 convolutions. The FCN structure also uses skip connections between layers, which improves performance. A kernel regularizer is used at each layer, which drives most weights to zero, significantly improving the recognition. Also, normal-distributed random values are used to initialize the weights of the decoder part.

### Parameters

A number of parameter sets was tested, and the following values appeared to deliver better performance:
- Kernel regularizer weight: 2e-3
- Normal initializer std. dev.: 0.012
- Batch size: 4
- Number of epochs: 50
- Keep probability: 0.45
- Learning rate: 0.0007
- Optimizer: Adam Optimizer

### Results

The average loss at the end of optimization process is around 0.02-0.04.
The following images are presented to visualize the model perofrmance in different cases. Although most of the road pixels are marked correctly, there are some false positives.

![1](./um000013.png)
![2](./um000029.png)
![3](./um000051.png)
![4](./um000061.png)
![5](./um000072.png)
![6](./um000085.png)
![7](./umm000007.png)
![8](./umm000069.png)
![9](./uu000052.png)
![10](./uu000069.png)
