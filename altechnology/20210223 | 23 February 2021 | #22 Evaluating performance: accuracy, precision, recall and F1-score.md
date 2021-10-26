[![#22 Evaluating performance: accuracy, precision, recall and F1-score](https://i.ytimg.com/vi/WiN5JCueeFQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=WiN5JCueeFQ)

## #22 Evaluating performance: accuracy, precision, recall and F1-score

In this video, I introduce you to basic metrics for evaluating the performance of natural language processing models – accuracy, precision, recall and F1-score – and how they can be calculated using the scikit-learn library for Python.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/05_evaluating_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=0) |  Hi again! In this video I'm going

to tell you about how to evaluate the performance of natural language processing models. Once we have a reliable gold standard at hand, we can use the gold standard to measure the performance of natural language processing models. Next I'm going to define a toy example consisting of two Python lists named "gold_standard" and "predictions" that then stand in for the gold standard and the predictions made by some language model,  

#### [0:00:30](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=30) |  and I assign them to these two

lists. Now that we have defined these two lists I'm going to import the metrics module from scikit-learn so we will have some metrics for evaluating the performance of the language model. I'm going to start by calculating accuracy between the gold standard and the predictions which is simply defined as the number of matches in the two lists and I'm going  

![](https://i.ytimg.com/vi/WiN5JCueeFQ/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=60) |  to do this by calling the accuracy_score

function from the "metrics" submodule of scikit-learn. This function takes two inputs, that is, the lists of items to be compared, and when I run this cell we get a value of 0.7 indicating 70 accuracy. To get a more comprehensive picture of model performance, we can use the classification_report function  

#### [0:01:30](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=90) |  which is available in the scikit-learn metrics submodule.

What I'm doing in this cell I'm calling the classification_report function and providing two inputs the list containing the gold standard and the list containing the predictions and I'm also putting in the keyword zero_division with a value of zero because this is needed to handle the cases where the predictions made are not present  

![](https://i.ytimg.com/vi/WiN5JCueeFQ/maxres2.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=120) |  in the gold standard. What we get

back is a neat table measuring the performance of the model, so let's continue by taking a closer look at this table. On the rows you have the unique categories present in the data, so in this case we have adjectives, auxiliary verbs, determiners and nouns, and so on and so forth. In the columns we have values for precision,  

#### [0:02:30](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=150) |  recall, F1-score and support. Precision tells you how

many of the predictions were correct for each class, or in this case a part of speech tag, so if you take a look at the row for adjectives you'll see that the value under the column position is 1, which means that the model was always correct when classifying adjectives. For nouns the model was only correct half the time, so the value is 0.5.  

#### [0:03:00](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=180) |  Recall gives the proportion of correct predictions for

all examples of a particular class. In other words, recall tells you how many instances of a given class or part of speech tag the model was able to find in the ground truth, so again if you take a look at the column for  

![](https://i.ytimg.com/vi/WiN5JCueeFQ/maxres3.jpg)



#### [0:03:30](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=210) |  adjectives you'll see that the recall is 0.67

which indicates that the model was able to correctly identify two thirds of the adjectives in the gold standard, or to put it differently the model missed one instance of an adjective in the gold standard. The F1 score is the harmonic mean of precision and recall, and it's intended to give you an overall  

#### [0:04:00](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=240) |  idea of how well the model performs in

terms of both precision and recall. Finally, the column for support gives you the number of instances for a given class present in the gold standard. At the bottom of the table you find average values for all of these metrics. The macro average is simply an average over all of the classes in the data and each class or category  

#### [0:04:30](https://www.youtube.com/watch?v=WiN5JCueeFQ&t=270) |  is considered equally important for the final score

The weighted average, in turn, takes into account the number of items in each category, so the scores are weighted according to the number of items which are shown in the column for support. Thanks for watching: I hope that you found this video useful and if you have any questions feel free to leave a comment below!  