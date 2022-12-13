# extend AI assessment
 ML Eng assessment project
 
This file serves as the readme file for Extend AI computer vision assessment. The first step in this project was to observe the given images and manually separate the cracked wood images from the uncracked ones in to two different folders. Following this, the directory of each folder is read in the python file and the unmarked folder holds a target value 0 while the marked holds target value 1.
In order to develop the best algorithm, first, the matrices i.e., RGB representing the cracked and the uncracked images are observed in order to come up with the best CNN architecture. The supplied data was too little for training, therefore, data augmentation was used to generate 640 data points for training. The data augmentation techniques involved rotation of the pixels and addition of noise. To ensure good generalization, the data points were shared equally between both classes. 
Images of the wood read was 128 by 128 by3 and with this attribute, CNN will be best for training a model. After trying different combinations, 6 filters worked the best with the first 3 input channels and 64 output channels while the last was a 256 input channels and 128 output channels. Three fully connected layers followed this. No padding was used since the cracks in the wood were not at the edges. Thus, a stride of 1 and kernel of size 3 were decent. It is worthy to mention that other architectures are possible with the CNN and based on my experiment, 6 convolutional layers provide a good enough performance. In addition, learning rate (lr) was critical to training the model and for this work lr of 0.0001 provided the best performance. 
In carrying out training, only the augmented data was used while the real data that was supplied was used for validating the trained model. The model accuracy based on this was 100%.
The last part of this project was the bounding box and I am still working on this.
