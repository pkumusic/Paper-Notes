## Idea: Can this be used to count-based exploration in DRL?

## Main points
* Model joint probability as a product of conditional probabilities.
* Model pixels as discrete variables with softmax output layer
* Use residual connections
* Diagnonal BiLSTM based PixelRNN performs best in the experiment

## Experiments
* Datasets: MNIST, CIFAR, IMAGENET
* Evaluation: Negative Log Likelihood around 3.0
* 32 x 32 and 64 x 64 images
