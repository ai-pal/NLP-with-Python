# Guide to NLP using Python :sunglasses:

This repository focuses on **NLP (Natural Language Processing)** using the Python Language.

## Contents

`News-Classifier` notebook focus on categorizing news articles by processing the body of the content. 

You can tweak the code a bit to improve the accuracy of the predictions by combining both Body and Title for processing. 

## Steps to Run

First clone the repository.

```sh
git clone https://github.com/DevDHera/Guide-to-NLP-with-Python.git
```

Now open the juputer notebook and classify news articles to your choice.

All the data sets are included inside `dataset` directory.


## Tech Stack

Following are some of the packages we use to build our classifier.

* nltk - Stopwords, Stemming
* pandas - To read TSV, create dataframes
* matplotlib, seaborn - Data visualizations
* string - To remove punctuations
* sklearn - CountVectorizer, TfidfTransformer, MultinomialNB, Pipeline

## Code Samples

We import the data into notebook like below.

``` python
news = pd.read_csv('dataset/trainset.txt', sep='\t', names=['CLASS', 'TITLE', 'DATE', 'BODY'])
```

Also, we use pipelines to make our life easier :sleeping:.

``` python
pipeline = Pipeline([
    ('bow', CountVectorizer(analyzer=text_process)),
    ('tfidf', TfidfTransformer()),
    ('classifier', MultinomialNB())
])
```

Improve the classifier and :heart: share the knowledge :bouquet: :blush: 