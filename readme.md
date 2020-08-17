# Neural Benford
This repository contains a Jupyter notebook that investigates whether the leading digit of a trained neural network obeys Benford's law.

## Benford's Law
From the [Wikipedia page](https://en.wikipedia.org/wiki/Benford%27s_law), Benford's Law "states that in many naturally occurring collections of numbers, the leading significant digit is likely to be small. For example, in sets that obey the law, the number 1 appears as the leading significant digit about 30% of the time, while 9 appears as the leading significant digit less than 5% of the time. If the digits were distributed uniformly, they would each occur about 11.1% of the time."

![Benford's Law Distribution](https://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Rozklad_benforda.svg/768px-Rozklad_benforda.svg.png)

## Initial Results

### First layer leading digit distribution vs. Benford's Law
Before Training
![Before training](https://github.com/alxcnwy/neuralbenford/blob/master/plots/before_layer1.png?raw=true)
After Convergence
![After training](https://github.com/alxcnwy/neuralbenford/blob/master/plots/after_layer1.png?raw=true)

### All layers leading digit distribution vs. Benford's Law
Before Training
![Before training](https://github.com/alxcnwy/neuralbenford/blob/master/plots/before_layers.png?raw=true)
After Convergence
![After training](https://github.com/alxcnwy/neuralbenford/blob/master/plots/after_layers.png?raw=true)

## Next steps
- [ ] Perform goodness-of-fit distribution tests 
- [ ] Evaluate a range of different architectures
- [ ] Compare different weight initializations 