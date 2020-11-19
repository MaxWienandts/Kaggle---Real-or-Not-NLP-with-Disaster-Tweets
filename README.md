# Kaggle---Real-or-Not-NLP-with-Disaster-Tweets
Natural Language Processing model using spaCy

As the Titanic model, this project is to familiarize with the basic tools of Python regarding natural language processing.
Again, any of the model used here are state of the art.
The model used in this projects are: naive Bayes; logit; random forest. 
Best score on Kaggle (naive Bayes): 0.77811

However, these models are extremely limited.
First of all, it was used a unigram bag of words. This has a huge drawnback of considering that one word does not modify another.

Second, we did not have a full dictionary to map the words. Here we used as vocabulary only the words that appeared in our train database.
This turns our model useless in front of any new word.
The correct would be to have a full dictionary and group the new words (that does not appear in our train) with similar words that we know how to classify.
E.g., if we only have flood in our train, we could consider the words inundation and alluvion as having the same probabilities as flood.

Lastly, to solve natural language processing problems, the most adequate is to use neural networks.
For instance, the use of recurrent nerual network would greatly increase the performance of our model.
RNN have the advantage of considering the whole sentence and not only one word in separate. 
This fact alone may be a disadvantage because the model would not be able to identify similar sentences with small variations.
However, this can be fixed using a layer with dropout. This layer "forgets" part of the sentence to avoid overfit.
Moreover, RNN applies the same weight vector for all layers. This simulate an effect of the model identifying the key words of a sentence, and the sentences "The forest is in fire" and "A fire in the forest" would have the same classification.
