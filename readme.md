## NLP ENGLISH TO YORUBA USING TRANSFORMER  --ATTENTION IS ALL YOU NEED

Transformer is totally based on attention using normal Linear layers, thereby eradicating the use of rnn in during sequence to sequence. One amazing stuff about RNN and LSTM is that sequence are represented as `time-steps` , hence their is sequence order. Instead transformer used `Postitional Encoding` to create orderliness in sequence. The positonal encoder involve encoding the odd postional with `sine function` and the even position of the sequence is represented with `cosine function` am thinking this is done because of the trigonometry property of sine being an `odd function` and cosine being an `even function`. This postional encoder is added with the embedded matrixsince they are of the same dimension.

The matrix `query`, `key` and `value` are all the same for self-attention and only the `value` is different for multihead attention since is coming from the encoder. The transformer consist lot of cool techniques like `Label smoothing` to make the model not to be too sure. Planning of **Writing a blogpost on it* Winks

## The Process

I make use of the havard NLP [post](http://nlp.seas.harvard.edu/2018/04/03/attention.html). which make use of english to french, they use spacy tokenization to tokenize both language. Since the tokenization for yoruba is not available, i was able to tokenize the English and Yoruba language using a custom function thanks to this pytorch [tutorial](https://pytorch.org/tutorials/intermediate/seq2seq_translation_tutorial.html) for the heads up, most of their utility function was used.

In the tutorial pytext batching was used in relation to spacy, and since am not using spacy a custom batchong is needed, i used` TensorDataset` and `DataLoader`.

### Data generation

The data was generated from jehova withness (english and yoruba) bible epub version. The data generation was made easy by following through the same process used by a cooleague Goodness Duru who assisted in generating the dataset for the IGBO Dataset.

The Transformer architecture is amazing, i did not train it with single words but it was able to translate single words and it is very fast. 

Truly **Attention is all you need** ;)

Much contribotion from a brother Steve Oni
