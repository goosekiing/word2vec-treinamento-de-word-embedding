# Word2Vec: Treinamento de Word Embedding

This repository contains a project focused on training Word2Vec models using a dataset of news titles and texts in Brazilian Portuguese from various websites, classified into categories: columns, daily life, sports, illustrated, market, and world.

## Project Overview

### Part 1: Training Word Embedding Models
The first part of this project aims to use the news titles to create Word Embedding models, which generate vector representations of words, capturing their semantics based on the context they appear in. The Word2Vec models created in this project are:

- **CBOW (Continuous Bag of Words) with 300 dimensions:** Attempts to predict the target word using the context and is generally faster.
- **SKIP-GRAM with 300 dimensions:** Attempts to predict the context using the target word and performs better with rare words.

The Spacy library is used for processing and tokenizing the titles, and the Gensim library is used to create and train the Word2Vec models. The generated models are saved in txt format.

### Part 2: Classifying News Titles
The second part of this project proposes using the models generated in the first part to classify news titles, determining their category. This is similar to what was done in the project "[Word2Vec: Interpretação da Linguagem Humana com Word Embedding](https://github.com/goosekiing/word2vec-interpretacao-da-linguagem-humana-com-word-embedding)", which used Word Embeddings models from NILC (Interinstitutional Center for Computational Linguistics).

Using the same method of summing vectors and classifying with a LogisticRegression model from the previous project, but with the CBOW and SKIP-GRAM models trained in the first part of this project, we achieve a classification accuracy of:

- **CBOW model:** 79%
- **SKIP-GRAM model:** 79%

Comparison with NILC models used in the project [Word2Vec: Interpretação da Linguagem Humana com Word Embedding](https://github.com/goosekiing/word2vec-interpretacao-da-linguagem-humana-com-word-embedding):

|              |   Accuracy   |   Accuracy    |     Size     |     Size      |
|     Model    | (Our Models) | (NILC Models) | (Our Models) | (NILC Models) |
|--------------|------------- |-------------- |--------------|---------------|
| CBOW         | 79%          | 80%           | 43MB         | 2.47GB        |
| SKIP-GRAM    | 79%          | 81%           | 43MB         | 2.47GB        |

- **Exported Models:** The classification models are exported in binary format using the pickle library.

## Course Details
This project was completed as part of the 'Advanced Machine Learning' course on Alura. For more information about the course, visit [Alura](https://cursos.alura.com.br/formacao-machine-learning-avancada).

## Objectives Achieved
- Learn how to use Spacy for text data preprocessing, including its advantages and disadvantages.
- Learn to configure the hyperparameters of the Word2Vec model.
- Train your own Word2Vec model using Gensim.
- Create a text classifier using your own Word2Vec model.
- Deploy your model in a web application.

## Technologies Used
- Python (v3.11.4)
- Jupyter Notebook
- Numpy
- Pandas
- Pickle
- Spacy
- Gensim
- Scikit-learn

## Project Structure
The directory structure of the project is as follows:
```
word2vec-treinamento-de-word-embedding/
│   modelo_cbow.txt
│   modelo_skipgram.txt
│   project-08-part-1.ipynb
│   project-08-part-2.ipynb
│   README.md
│   rl_cbow.pkl
│   rl_sg.pkl
```

## Setup Instructions
1. Clone the repository:
   ```sh
   git clone https://github.com/goosekiing/word2vec-treinamento-de-word-embedding.git
   ```
2. Navigate to the project directory:
   ```sh
   cd word2vec-treinamento-de-word-embedding
   ```
3. Create a virtual environment and activate it:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```
4. Install the required libraries:
   ```sh
   pip install numpy pandas pickle spacy gensim scikit-learn
   ```

## Running the Notebook
1. Open Jupyter Notebook:
   ```sh
   jupyter notebook
   ```
2. Run the `project-08-part-1.ipynb` and `project-08-part-2.ipynb` notebooks to see the Word2Vec model training and news classification in action.

## Dataset
The dataset used is the same as the one used in the previous project titled "Word2Vec: Interpretação da Linguagem Humana com Word Embedding," available at [this link](https://github.com/goosekiing/word2vec-interpretacao-da-linguagem-humana-com-word-embedding). The code is already configured to read the dataset directly from this GitHub repository without the need to download the CSV files.

## Language
The language used in this project is Brazilian Portuguese (pt-br).

## Author
GitHub Username: [goosekiing](https://github.com/goosekiing)
