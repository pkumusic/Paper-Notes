## Idea: DeepGAN? Can we stack multiple layers of GANs to generate better results?

## Main points
* Generate photo-realistic images condition on text description
* Stack two GANs to generate images in two steps.

## Experiments
* Datasets: Caltech-UCSD Bird and Oxford-102 flower
* Baselines: GANINT-CLS, GAWWN
* Evaluation Method: Inception score of generated images; Nearest Neighbor Retrieved to prove not memorizing; Linear Interpolation of sentence Embedding to see smooth image changing.
