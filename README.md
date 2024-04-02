# English to French Translation using PyTorch Transformer

This project implements a neural machine translation system to translate text from English to French using the Transformer architecture. The model is trained on a dataset of 163,765 English-French sentence pairs and evaluated using both quantitative and qualitative methods.

## Dataset

The dataset consists of 163,765 sentence pairs with English and corresponding French translations. It covers a range of topics and complexity levels, with sentence lengths varying from short phrases to longer descriptive sentences. The dataset is split into train, validation, and test sets of 147,000, 20,000, and 16,000 pairs, respectively.

## Model

The Transformer model comprises an encoder and decoder mechanism connected through attention layers. The implemented architecture has 6 layers in both the encoder and decoder, with multi-head attention mechanisms to capture dependencies within and between the input and output sequences. The model uses a token embedding size of 192 and is trained with a batch size of 128 for 50 epochs.

## Training

The model is trained to minimize the Cross-Entropy Loss between the predicted translations and the actual French sentences. The Adam optimizer is used to update the model's 14.5 million parameters during the training process.

## Results

The model's performance is evaluated through loss analysis on the training and validation sets, as well as qualitative human evaluation of sample translations.

### Loss Analysis

The training and validation losses exhibit a decreasing trend over the 50 epochs, reaching final values of 1.2 and 1.3, respectively. This indicates that the model effectively learned from the training data and generalized well to unseen examples.

### Translation Analysis

Qualitative evaluation by native French speakers revealed that the model performs well on simple sentences with common vocabulary and basic grammar. However, performance degrades on longer, more complex sentences, exhibiting issues with fluency, nuanced meaning preservation, vocabulary coverage, and proper word ordering.

## Conclusion

While the Transformer model demonstrates fundamental translation capabilities, further improvements are needed to address gaps in coherence, precision, vocabulary, and syntactic ordering. Expanding the training data and fine-tuning the model architecture are potential avenues for future work to enhance translation quality.

## References

1. Johnson et al. Google's multilingual neural machine translation system. arXiv 2016
2. Liu et al. Towards Robust Neural Machine Translation. arXiv 2018.
3. Vaswani et al. Attention is all you need. NeurIPS 2017.
4. Wu et al. Google's neural machine translation system. arXiv 2016.
5. Papineni et al. BLEU: a method for automatic evaluation of machine translation. ACL 2002.
