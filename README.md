# COVID-19 Question Answering System

The COVID-19 Question Answering System is designed to provide answers to user queries related to COVID-19 using a fine-tuned RoBERTa model. The system consists of three main components: knowledge base, retriever, and reader.

## Prerequisites

- Python 3.x
- pandas
- Haystack library
- Elasticsearch
- sentence-transformers library

## Installation

1. Clone the repository:

         git clone https://github.com/marwankhaled1/covidQA
         cd covid-qa-system

2. Install the required dependencies:
      
         pip install pandas
         pip install git+https://github.com/deepset-ai/haystack.git


3. Download the pre-trained RoBERTa model for question answering and place it in the project directory.

## Preprocessing

The `preprocessing.ipynb` notebook contains the preprocessing steps for the dataset used in fine-tuning the RoBERTa model. It includes tasks such as removing unnecessary columns, handling missing values, removing punctuation, and lowercasing the data.

## Elasticsearch Setup

The `es_populate.ipynb` notebook sets up the Elasticsearch knowledge base and the retriever. It populates the knowledge base with research articles related to COVID-19 and updates the embeddings for efficient similarity matching. The notebook uses the ElasticsearchDocumentStore and EmbeddingRetriever from the Haystack library.

## Dataset

The `dataset` directory contains a sample of the dataset used to fine-tune the RoBERTa model. The dataset consists of COVID-19 related questions and their corresponding answers.

## Usage

To use the COVID-19 Question Answering System:

1. Make sure the Elasticsearch service is up and running.

2. Run the `es_populate.ipynb` notebook to set up the knowledge base and retriever.

3. Once the knowledge base is populated and the embeddings are updated, you can use the system to answer questions. Modify and run the appropriate code in the notebook to interact with the system.

4. The system will take a user query, pass it through the retriever to retrieve relevant research articles, and then use the reader to extract answers from the retrieved articles.

5. The system will return the extracted answers along with any supporting context or source information.

## Performance

The fine-tuned RoBERTa model achieves an accuracy of 91.8% and an F-measure of 91.26% on the COVID-19 question answering task. The model has been trained on a dataset specifically curated for COVID-19 related questions.


