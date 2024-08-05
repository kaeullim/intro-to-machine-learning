# Intro to Machine Learning

## Deep Learning (DL)

### Convolutional Neural Networks (CNNs)

## Large Language Models (LLMs)

### Transformers
  * [Transformers](https://github.com/huggingface/transformers)
    
### Bidirectional Encoder Representations from Transformers [BERT](https://huggingface.co/docs/transformers/en/model_doc/bert)
  * Pretrained models: BERT base model (uncased) [bert-base-uncased](https://huggingface.co/google-bert/bert-base-uncased)
   - Model description: BERT is a transformers model pretrained on a large corpus of English data in a self-supervised fashion with two objectives:
     1. Masked language modeling (MLM): taking a sentence, the model randomly masks 15% of the words in the input then run the entire masked sentence through the model and has to predict the masked words. This is different from traditional recurrent neural networks (RNNs) that usually see the words one after the other, or from autoregressive models like GPT which internally masks the future tokens. It allows the model to learn a bidirectional representation of the sentence.
     2. Next sentence prediction (NSP): the models concatenates two masked sentences as inputs during pretraining. Sometimes they correspond to sentences that were next to each other in the original text, sometimes not. The model then has to predict if the two sentences were following each other or not.
   ```
   model = BertForSequenceClassification.from_pretrained('bert-base-uncased', num_labels=num_labels)
   ```
  * Fine Tuning: selection of optimized parameters (max_length, batch_size, num_epochs)
  * Tokenization: language model predicts next token using given tokens
   ```
   tokenizer = BertTokenizer.from_pretrained("bert-base-uncased")
   ```
  * Optimizer: AdamW
  * Attention

### eXtra Gradient Boost [XGBoost](https://xgboost.readthedocs.io/en/stable/python/python_intro.html)
XGBoost is an implementation of gradient boosted decision trees designed for speed and performance that is dominated by competitive machine learning.

## Introduction to Python
* Introduction of Pandas, [see this document](Basic-Pandas.md)
  
### Study Plan
 * Leetcode Problems [Top Interview 150](https://leetcode.com/studyplan/top-interview-150/)
 * Leetcode Problems [LeetCode 75](https://leetcode.com/studyplan/leetcode-75/)
 * Leetcode Problems [Introduction to Pandas](https://leetcode.com/studyplan/introduction-to-pandas/)

