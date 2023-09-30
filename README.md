# What is this project 

This project allows you to use Chat GPT's APIs to ask questions about a PDF. It implements Retrieval Augmented Generation 
by precomputing text embeddings of pages of a PDF. Then, given a user query, we perform a local search for all relevant pages and send them up as context to the chat GPT API. 

NOTE: This requires that you have an (OpenAI API key)[https://openai.com/blog/openai-api]. This will cost some money 💵 depending on what model you select. If you use the provided example PDFs and play around with it a few days it should cost you less than a couple of dollars. 

TODO: More details about the architecture soon.

# How to set up your environment 

We recommend you use venv to install and isolate your dependencies: 

```
python3 -m pip install --user virtualenv
python -m venv env 
source ./env/bin/activate       #NOTE: In Windows, directories are slightly different
python -m pip install -r requirements.txt
```

# How to use the code

There's two main python notebooks to run 

- 00_generate_embeddings.ipynb: This will create a local csv file containing text embeddings for all pages in your PDF 
- 01_ask_questions.ipynb: Use this after creating the embedding to answer questions about your PDF. This code sends up relevant text up to the OpenAI Chat API in order to retrieve an answer. 

The files have exposed various parameters that you can play with.

# What's the data in this folder?

- BT_Core_v5.4 : Bluetooth Core Specification document, a good non-trivial document to ask questions about. 

- BT_Core_v5.4.mini : ~15 page extract of **BT_Core_v5.4** that you can use for speedy development.


