# Neural Benford
<<<<<<< HEAD
Benford's law is a fascinating property that applies to many naturally occuring numbers that the leading digit distribution follows a non-uniform skewed distribution. It has been shown to apply to a wide variety of datasets including electricity bills, stock prices, lengths of rivers, Fibonacci numbers and the factorials, among others.
           
This repository contains a Jupyter notebook investigating whether the leading digits of weights in a neural network follow Benford's Law.

It appears that the weights of a network do not follow Benford's Law before training but do approximately follow Benford's Law after convergence and then deviate from Benford's Law when the model starts overfitting.

![Neural Benford](https://github.com/alxcnwy/neuralbenford/blob/master/plots/benford.gif?raw=true)

A surprising result is that it appears that model Validation Accuracy is maximised around the time when the leading digit MAD vs. Benford's Law is minimized! This has observed with MNIST & Fashion MNIST with several different architectures but needs to be explored on more architectures and datasets.

![Accuracy vs. Benford Weight MAD](https://github.com/alxcnwy/neuralbenford/blob/master/plots/accuracy_vs_mad.jpg?raw=true)


## Benford's Law
From the [Wikipedia page](https://en.wikipedia.org/wiki/Benford%27s_law), Benford's Law "states that in many naturally occurring collections of numbers, the leading significant digit is likely to be small. For example, in sets that obey the law, the number 1 appears as the leading significant digit about 30% of the time, while 9 appears as the leading significant digit less than 5% of the time. If the digits were distributed uniformly, they would each occur about 11.1% of the time."

![Benford's Law Distribution](https://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Rozklad_benforda.svg/768px-Rozklad_benforda.svg.png)

Here's a [great Numberphile video](https://www.youtube.com/watch?v=XXjlR2OK1kM) talking about Benford's Law.


## Experiment Details
I compared the leading weight digit distribution before and after training convergence of a convolutional neural network architecture adapted from the [Keras documentation](https://keras.io/examples/vision/mnist_convnet/). I compared the distributions of weights in just the first layer and all layers in the network for MNIST and Fashion MNIST.

The leading digit was calculated by ignoring the weight sign and taking the first non-zero digit in the weight value.

## Directions for Future Work
- [x] Plot mean deviance over time as the network is trained
- [ ] see if sampling starting weights from Benford's law improves convergence
- [ ] Check if results hold for different architectures/datasets
- [ ] Perform goodness-of-fit distribution tests 
- [ ] Compare different weight initializations
- [ ] Return weight statistics before/after training
- [ ] Investigate using deviation as a measure of network fit

Inspired by [this Reddit thread](https://www.reddit.com/r/learnmachinelearning/comments/ibesos/the_weights_of_my_first_hidden_layer_start_to/).
