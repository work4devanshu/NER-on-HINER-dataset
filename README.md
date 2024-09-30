# Traditional Methods for Hindi Named Entity Recognition (NER)

This repository contains the implementation of traditional machine learning methods applied to the Hindi Named Entity Recognition (NER) task. The project utilizes well-known classifiers such as Decision Tree, Random Forest, and Support Vector Machine (SVM) to extract and classify named entities.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
4. [Feature Engineering](#feature-engineering)
5. [Model Training and Evaluation](#model-training-and-evaluation)
6. [Performance Evaluation](#performance-evaluation)
7. [Conclusion](#conclusion)
8. [Future Scope](#future-scope)
9. [References](#references)

## Introduction

Named Entity Recognition (NER) is a crucial task in Natural Language Processing (NLP) used to identify and categorize entities such as person names, locations, organizations, and temporal expressions. In this project, we explore traditional machine learning methods to perform NER on Hindi text using the **HiNER dataset**. The goal is to evaluate the effectiveness of these methods compared to modern deep learning models.

### Applications of NER:
- Information Retrieval
- Question Answering
- Sentiment Analysis

NER helps improve text understanding by categorizing entities and facilitating better semantic comprehension.

## Dataset

The **HiNER dataset**, available from the `datasets` library, is specifically designed for Hindi NER tasks. It includes a variety of annotated named entities. We divided the dataset into two parts:
- **Training Set**: Used for model training.
- **Test Set**: Used for evaluating model performance.

## Methodology

### Data Acquisition
We used the HiNER dataset for training and testing. The dataset is annotated and specifically curated for NER tasks in the Hindi language.

### Data Preprocessing
To prepare the data for machine learning models, we performed several preprocessing steps:
- **Tokenization**: Splitting text into individual tokens.
- **POS Tagging**: Annotating each token with its part-of-speech (POS) tag using the StanfordNLP library.
- **Data Limiting**: We limited the dataset to 2000 entries for both training and testing due to computational constraints.

## Feature Engineering

To enhance model performance, the following features were engineered:
- **POS Tags**: These provide syntactic information about the role of each word.
- **Binary Indicators**: Features indicating the beginning (BOS) or end (EOS) of a sentence.
- **Contextual Features**: The words immediately surrounding each token were included as features.

## Model Training and Evaluation

We trained three traditional machine learning models on the extracted features:
1. **Decision Tree Classifier**
2. **Random Forest Classifier**
3. **Support Vector Machine (SVM)**

Each model was evaluated using precision, recall, and F1-score as performance metrics. Confusion matrices were generated to visually assess performance across different named entity categories.

## Performance Evaluation

The evaluation metrics used in this project include:
- **Precision**
- **Recall**
- **F1-Score**

Below is a comparison of our results with those of the base paper.

### Base Paper Results
The base paper utilized modern deep learning methods and significantly outperformed traditional machine learning methods due to the limitations of the latter in capturing sequential data.

### Our Results
We observed that traditional methods, while useful for extracting basic patterns, were not as effective in handling sequential and contextual dependencies in the dataset.

## Conclusion

Our experiments demonstrated that:
- **Base paper models significantly outperform traditional methods** due to their ability to capture sequential patterns and contextual dependencies.
- Traditional methods rely heavily on handcrafted features, which can be limiting.

### Challenges:
- Limited training data due to computational constraints.
- Lack of sophisticated feature engineering support for regional languages like Hindi.

## Future Scope

1. **Temporal Dependencies**: Implement models that can capture temporal dependencies in the data.
2. **Contextual Understanding**: Use models that can understand the contextual nature of tokens.
3. **Improved Feature Engineering**: Enhance feature extraction by adding morphological features.
4. **Broader Applications**: Generate text classification or sentiment analysis datasets from the HiNER dataset.

## References

1. A. A. Awan, "What is Named Entity Recognition (NER)?", [Datacamp](https://www.datacamp.com/blog/what-is-named-entity-recognition-ner).
2. R. Murthy et al., "HiNER: A Large Hindi Named Entity Recognition Dataset", [HiNER Paper](https://www.cse.iitb.ac.in/~pb/papers/lrec22-ner.pdf).
3. "stanfordnlp/stanza", [GitHub](https://github.com/stanfordnlp/stanza).

