A good explanation: https://jalammar.github.io/illustrated-transformer/

Self-attention instead of recurrent connection (RNN) or CNN (usually only positional info but no weights related to content similarity).
* Easy for training parallelization
* Decoding still cannot be parallellized in inference (can be parallelized in training through 
teacher-forcing, where ground truth word is used while training instead of the predicted word.)

Important Techniques
* Attention: 
  * Q (query), K (Key), Value (V), use Q to query K, softmax, and weighted sum of value.
  * Q, K, V is basically a projection of original input embedding to another subspace through matrix mult, matrix weights are learnable.
* Multi-head: similar to channels to CNN, can generate subspaces for feature representation
(interesting findings including one head always looking at the leading subject/verb, and another head always try correference resolution)
* Forward-looking mask for decoder
* Positional encoding: Unparameterized, sine and cosine funtions.

Caveat
* self-attention caculates softmax for one word on all words in the sequence. What if the sequence is very long?
* Decoder is still "recurrent" (any ways to improve? for a human we probably just come up with key words and then make a sentence around it)

Training
* BPE (byte-pair encoding) for subword splitting
* Adam optimizer
* Residual links, dropout, batch norm

Promising results as all known.
