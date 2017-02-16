# main points 
* Introduce a way to project images into word embedding space. Actually very simple. Use the word embedding info for synonyms.
* Pretrain skip-gram word embedding model
* Pretrain CNN with a softmax output layer to predict 1000 classes
* The visual model is used to predict the word embeddings
* It is actually project the iamges into word embedding spaces and minimize the ranking cosine distance.
* Loss can also be backpropogated to visual model(CNN) to improve accuracy by 1% ~ 3%
