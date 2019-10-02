# Stacking Models Like a Pro



# The problem

Mail routing for a medium sized? Danish Pension Fund. A pension fund recieves a large amount of customer emails or messages through
custom apps and homepage forms, which need to be rerouted to the relevant departments.
At the time of writing, this process is manual and handled by the entry point for mails, i.e. the customer service department.

This is a labour intensive and error prone process. The task at hand was to build a model to automate this rerouting process.
The model would recieve an email or customer enquiry, then classify it according to a set of categories representing distinct
workflows within the company, and then forward the enquiry accordingly.


# Anonymizing the data

The data itself posed an additional challenge. Being customer enquiries to a Pension Fund, the information contained in these
messages is incredibly sensitive. WHY IS THIS BAD?

As a precondition for us even engaging in the project was that this data is anonymized. To achieve this we processed all the mails
with our custom Named Entity Recognition [BERT](https://github.com/google-research/bert) model.

For this we use the wonderful PyTorch implentation by [Huggingface](https://github.com/huggingface/transformers).



# The architecture

# How it was trained

# Using BERT for text classification.


