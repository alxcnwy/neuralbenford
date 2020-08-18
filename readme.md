# Neural Benford
Benford's law is a fascinating property of many naturally occuring numbers that the leading digit distribution follows a non-uniform skewed distribution. It has been shown to apply to a wide variety of datasets including electricity bills, stock prices, lengths of rivers, Fibonacci numbers and the factorials, among others.

This repository contains a Jupyter notebook investigating whether the leading digits of weights in a neural network follow Benford's Law.

It appears that the weights of a network do not follow Benford's Law before training but do approximately follow Benford's Law after convergence...

Inspired by [this Reddit thread](https://www.reddit.com/r/learnmachinelearning/comments/ibesos/the_weights_of_my_first_hidden_layer_start_to/).

An interesting possible direction of research is how the leading digit distribution of weights at a point in time can be used as a measure for the network's fit without reference to a validation set.

![Neural Benford](https://github.com/alxcnwy/neuralbenford/blob/master/plots/benford.gif?raw=true)

## Benford's Law
From the [Wikipedia page](https://en.wikipedia.org/wiki/Benford%27s_law), Benford's Law "states that in many naturally occurring collections of numbers, the leading significant digit is likely to be small. For example, in sets that obey the law, the number 1 appears as the leading significant digit about 30% of the time, while 9 appears as the leading significant digit less than 5% of the time. If the digits were distributed uniformly, they would each occur about 11.1% of the time."

![Benford's Law Distribution](https://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Rozklad_benforda.svg/768px-Rozklad_benforda.svg.png)

Here's a [great Numberphile video](https://www.youtube.com/watch?v=XXjlR2OK1kM) talking about Benford's Law.


## Initial Experimental Results
I compared the leading weight digit distribution before and after training convergence of a convolutional neural network architecture adapted from the [Keras documentation](https://keras.io/examples/vision/mnist_convnet/). I compared the distributions of weights in just the first layer and all layers in the network. 

The leading digit was calculated by ignoring the weight sign and taking the first non-zero digit in the weight value.

#### First layer leading digit distribution vs. Benford's Law

![Before training](https://github.com/alxcnwy/neuralbenford/blob/master/plots/before_layer1.jpg?raw=true)

![After training](https://github.com/alxcnwy/neuralbenford/blob/master/plots/after_layer1.jpg?raw=true)

___

#### All layers leading digit distribution vs. Benford's Law

![Before training](https://github.com/alxcnwy/neuralbenford/blob/master/plots/before_layers.jpg?raw=true)

![After training](https://github.com/alxcnwy/neuralbenford/blob/master/plots/after_layers.jpg?raw=true)


## Directions for Future Work
- [x] Plot mean deviance over time as the network is trained
- [ ] Compare different weight initializations
- [ ] Perform goodness-of-fit distribution tests 
- [ ] Check if results hold for different architectures/datasets
- [ ] Investigate using deviation as a measure of network fit
- [ ] Return weight statistics before/after training

