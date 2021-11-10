After preprocessing almost 8,000 U.S. Supreme Court case opinions from 1968 - present, I built an LDA model using sklearn with a base model of 10 topics using CountVectorizer. I tuned the parameters of the CountVectorizer to be 0.05 min_df, 0.5 max_df and an ngram range between 1 and 3. 

To visualize the topics, I used pyLDAvis and found a lower relevance metric made the topics more clear, since at a higher lambda the words were highlevel law terms, e.g. case, action, motion, judge, court, etc. I also created graphical representation of the top 20 terms in each topic shown below. ![LDA_topics](https://user-images.githubusercontent.com/84474016/141164576-7e75ada2-5693-4c82-91c6-491ed8623e28.png)


Next, I plan to hypertune the parameters of the LDA model and try CorEx as an alternative topic modeling technique. In addition to topic modeling, I plan to build an unsupervised clustering model, namely Kmeans Clustering. 
