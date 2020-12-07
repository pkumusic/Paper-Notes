Glass-box approach using features from encoder-deconder NMT models 
* The output probability distribution from the NMT system
* The attention mechanism used during decoding

Assumption: More confident the decoder is, the higher the quality of the translation.

Interesting points:
* While sequence-level probabilities of the top MT hypothesis have been used for confidence estimation in statistical MT 
are generally not well calibrated, i.e. not representative of the true likelihood of the predictions.
* Softmax output probablities tend to be overconfident.

Dataset:
* New dataset with 6 language pairs representing high/medium/low resource. From Wikipedia documents, 10K segments per language pair. 
* Useing Direct Assessment of MT quality, basically assigning 1-100 scores instead of using HTER. 
* 3 annotator per setence.
* 7K training, 1K dev, 2 1K test sets.


Method:
* Softmax distribution
    * Top-1 average logp (force-decoding score)
    * Average entropy of softmax output distribution for each decoding step
    * Standard deviation of word-level logp
* Quantifying Uncertainty
    * Monte Carlo dropout 
* Attention
    * Entropy of the attention distribution

Experiments
* 4 groups, 1-Softmax, 2-MC dropout, 3-Attention, 4-Supervised
* MC Dropout seems performing well on several languages. Better than FDS in most cases.
