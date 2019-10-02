# Stacking Models Like a Pro

- [Stacking Models Like a Pro](#stacking-models-like-a-pro)
- [The problem](#the-problem)
- [Anonymizing the data](#anonymizing-the-data)
- [The ToolBox](#the-toolbox)
- [The architecture](#the-architecture)
- [How it was trained](#how-it-was-trained)
- [Using BERT for text classification.](#using-bert-for-text-classification)

# The problem

Mail routing for a medium sized? Danish Pension Fund. A pension fund recieves a large amount of customer emails or messages through
custom apps and homepage forms, which need to be rerouted to the relevant departments.
At the time of writing, this process is manual and handled by the entry point for mails, i.e. the customer service department.

This is a labour intensive and error prone process. The task at hand was to build a model to automate this rerouting process.
The model would recieve an email or customer enquiry, then classify it according to a set of **14** categories representing distinct
workflows within the company, and then forward the enquiry accordingly.


# Anonymizing the data

The data itself posed an additional challenge. Being customer enquiries to a Pension Fund, the information contained in these
messages is incredibly sensitive. WHY IS THIS BAD?

As a precondition for us even engaging in the project was that this data is anonymized. To achieve this we processed all the mails
with our custom Named Entity Recognition [BERT](https://github.com/google-research/bert) model.

For this we use the wonderful PyTorch implentation by [Huggingface](https://github.com/huggingface/transformers).

# The ToolBox

1) A danish spaCy model we trained ourselves using the **INSERT DATASET**, used for tokenization and PosTagging. We have attached the Danish lemmatizer [lemmy](https://github.com/sorenlind/lemmy) to the spaCy pipeline.
2) Sklearn. Several models from Sklearn, and most importantly pipelines from Sklearn. Sklearn has developed a very neat API for estimators and transformers, which we make sure to conform to whenever we write our own transformers and estimators. This makes sure that we can use our own transformers and estimators with in SKlearn Pipelines.
3) The Pytorch Transformers library by [Huggingface](https://github.com/huggingface/transformers).
4) 


# The architecture

# How it was trained

We had 7 models in layer 1. 


# Using BERT for text classification.


