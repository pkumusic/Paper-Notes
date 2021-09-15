Bidirectonal Encoder Representations from Transformer

* Masked language model for utilizing bidirectional (contextual) info.
* Next sentence prediction

BERT(base): 12 Layers, 768H, 12 Heads, 110M Params.
BERT(large): 24 layers, 1024H, 17 Heads, 340M Params.

Compared to Hybrid v2 (800M Parameters HBM -> 4 bytes per parameter if float -> 200M params). 
- 12 layers of transformer encoders (1024, 16 Heads), 2 layers of LSTM decoders (with attention)

* [CLS] and [SEP] tokens. 
* Input embedding = Token embeddings + segment embeddings (belong to first sentence or second sentence after [SEP]), positinoal embeddings.
* [MASK] token for Masked LM.
* Binary next sentence prediction. 
* Bert transfers all params to end-task model, while previously only sentences embeddings were used.  

Great exp results as known.
