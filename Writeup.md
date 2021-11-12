# Supreme Court Opinions: A Jumble of Words

## Abstract
The goal of this project is to build a topic modelling pipeline investigating U.S. Supreme Court case opinions that can aide legal professionals in finding potential case law precedents and academics looking to explore the judicial branch in the modern political era and probe hidden semantic relationships within the cases themselves. 

## Design
Using Supreme Court case opinions from the past fifty years available on FindLaw.com, I was able to build and tune a series of topic models using a variety of count vectorization techniques. 

## Data
The data was acquired by web-scraping [FindLaw's Library of U.S. Supreme Court case opinions](https://caselaw.findlaw.com/court/us-supreme-court) from 1968 to present. The dataset contains 7,916 U.S. Supreme Court Case opinions, ranging from 23 to 564,459 words with a median of 28,064 words. After removing duplicates, the dataset contained opinions for 7,741 cases. 

## Algorithms

*Text Preprocessing*
1. Removed footnotes and in text citations
2. Fixed Unicode encoding errors with ftfy 
3. Removed '\n', punctuation, numbers and custom stop words (nltk.english + 1000 most common words in English)
4. Converted all characters to lowercase 
5. Applied lemmatization with NLTK


*Models*
  
LDA using CountVectorizer and TFIDFVectorizer along with LDA Multicore and CorEx were used before settling on LDA with TFIDF vectorization as the model performing the best topic modeling. 

## Tools
- Numpy and Pandas for data manipulation
- NLTK and gensim for NLP
- Scikit-learn, gensim for modeling
- Matplotlib for plotting
- pyLDAvis for visualizing

## Communication
In addition to this written document, I have created and presented slides and visuals. 
