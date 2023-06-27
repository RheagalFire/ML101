# Natural Language Processing

What are word Embeddings and why do we need it?

Word Embeddings represent words in vectors and they are required because we can't perform computations on words itself. This is pretty basic. Now we can convert those words to their one hot encoded form where we stack all words together and mark the pos of the correct word as one. Two famous Libraries that provide embeddings are given below.&#x20;

1. Word2Vec: Word2Vec is a shallow neural network-based model that learns word embeddings by predicting neighboring words given a target word or vice versa. There are two main architectures in Word2Vec: Continuous Bag of Words (CBOW) and Skip-gram.&#x20;

* CBOW: The CBOW model predicts the target word based on its surrounding context words. It takes a fixed-size window of words around the target word and tries to predict the target word based on this context. The input to the CBOW model is the one-hot encoded vectors representing the context words, and the output is the one-hot encoded vector representing the target word. The model is trained to minimize the loss between the predicted target word and the actual target word.
* Skip-gram: The Skip-gram model, on the other hand, predicts the surrounding context words given a target word. It takes a target word as input and tries to predict the words within a fixed-size window around the target word. Similar to CBOW, the input and output vectors are one-hot encoded. The model is trained to minimize the loss between the predicted context words and the actual context words.

2. GloVe: GloVe is a global matrix factorization-based model that constructs word embeddings by factorizing the co-occurrence matrix of words. It leverages the statistical information about the frequency of word co-occurrences across the corpus to create meaningful representations.

The co-occurrence matrix captures how frequently words appear together in a given window of words. GloVe uses this matrix to build a low-dimensional vector space representation of words. The objective of GloVe is to find word embeddings that preserve the ratios of co-occurrence probabilities between words.

3. Projection onto 768 dimensions: Both GloVe and Word2Vec are typically trained on large corpora, which results in word embeddings with several hundred dimensions. The dimensionality is a hyperparameter that can be adjusted during training. The choice of 768 dimensions or any other specific number depends on the configuration set for training.

After training, the word embeddings in both algorithms are represented as dense vectors in this high-dimensional space. Each dimension in the vector captures some semantic or syntactic information about the word. These dimensions are learned during the training process and are not directly interpretable. The resulting 768-dimensional vectors are a compact representation of words that encode their relationships with other words in the corpus.

Please use this [link](https://analyticsindiamag.com/word2vec-vs-glove-a-comparative-guide-to-word-embedding-techniques/) to see what is unfolded with word2vec and GLove

