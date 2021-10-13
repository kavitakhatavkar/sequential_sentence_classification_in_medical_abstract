# sequential_sentence_classification_in_medical_abstract
**Aim** : Replicating the deep learning model behind the 2017 paper `PubMed 200k RCT: A Dataset for Sequenctial Sentence Classification in Medical Abstracts`.

**The goal of the dataset** was to explore the ability for NLP models to classify sentences which appear in sequential order.

In other words, given the abstract of a RCT, what role does each sentence serve in the abstract?

Example :
* inputs - (harder to read abstract from PubMed) and 
* outputs - (easier to read abstract) of the model we're going to build. 

The model will take an abstract wall of text and predict the section label each sentence should have.

**`Problem statement :`** 

> The number of RCT papers released is continuing to increase, those without structured abstracts can be hard to read and in turn slow down researchers moving through the literature.

**`Solution :`** 

Create an NLP model to classify abstract sentences into the role they play (e.g. objective, methods, results, etc) to enable researchers to skim through the literature and dive deeper when necessary.

**`Steps to be followed :`**

* Downloading a text dataset (PubMed RCT20k from GitHub)
* Writing a preprocessing function to prepare our data for modelling
* Setting up a series of modelling experiments
* Making a baseline (TF-IDF classifier)
* Deep models with different combinations of: 
  * token embeddings, 
  * character embeddings, 
  * pretrained embeddings, 
  * positional embeddings
* Building our first multimodal model (taking multiple types of data inputs)
* Replicating the model architecture from https://arxiv.org/pdf/1612.05251.pdf
* Find the most wrong predictions
* Making predictions on PubMed abstracts from the wild
