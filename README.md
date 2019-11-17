# Is Attention All You Need?
> An analysis on the trade-offs between NLP's standard neural models.

## Abstract
Transformer models have recently become the state of the art for a variety of natural language processing tasks (e.g. summarization, dialogue, translation). They offer computational benefits over standard recurrent and feed-forward neural network architectures, pertaining to parallelization and parameter size. In this paper, we analyze the performance gains of Transformer and LSTM models as their size increases, in an effort to determine when researchers should choose Transformer architectures over recurrent neural networks. 

## Related Work
The most prolific baselines for time-series and continuous data are recurrent neural networks, due to their ability to process sequential data. In particular, most tasks involve the use of LSTM (Long Short Term Memory) cells, which allows recurrent neural networks to learn long-term dependencies through the data, as well as preventing the vanishing gradient problem which plague standard RNN architectures. 

An improvement to the standard LSTM architecture is the mechanism of attention, which allows the network to calculate the importance of certain parts of the data (e.g. text), in relation to some other tertiary data (e.g. text). Attention-based architecture for neural machine translation was developed by Banhandau et. al in 2014 (?), and subsequently achieved state of the art performance in a variety of tasks, later becoming the gold standard for sequential processing. 

Transformer models are feedforward encoder/decoder architectures consisting of layers of self-attention. Transformer models were originally developed by Vastwani et. al in 2017, as a state of the art architecture for multilingual translation and have since been used in a variety of seq2seq tasks, including dialogue, summarization and named entity recognition. The importance of Transformer networks comes from their relative simplicity, consisting namely of feed-forward attention (without any recurrent units). This allows Transformer networks to train much larger volumes of data due to better parallelization. As such, Transformer models also benefit from larger parameter spaces, which can be tuned more accurately due to the increase of capacity of training data.

Although Transformer networks do claim the state-of-the-art, most implementations are very large (> 1 BILLION parameters) and are trained on corpi an order of magnitude larger than before. This makes it difficult to accurately compare performance gains of Transformer networks over those of LSTM networks. In this project, we aim to determine how the performance (both accuracy and efficiency) scale with both parameter size and corpus size.

## References
- https://arxiv.org/abs/1706.03762
- https://arxiv.org/abs/1910.01108
- https://arxiv.org/pdf/1909.11687.pdf
