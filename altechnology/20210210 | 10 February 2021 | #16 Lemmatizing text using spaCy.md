[![#16 Lemmatizing text using spaCy](https://i.ytimg.com/vi/pvMImQEUlN4/maxresdefault.jpg)](https://www.youtube.com/watch?v=pvMImQEUlN4)

## #16 Lemmatizing text using spaCy

In this video, I show you how to lemmatize text using spaCy.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/03_basic_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



![](https://i.ytimg.com/vi/pvMImQEUlN4/maxres1.jpg)



![](https://i.ytimg.com/vi/pvMImQEUlN4/maxres2.jpg)



#### [0:00:00](https://www.youtube.com/watch?v=pvMImQEUlN4&t=0) |  Hi again! In this video I'm going to

tell you about lemmatization using spaCy. Lemmatization refers to the process of returning words to their base form. This is very important because unless explicitly instructed, computers cannot tell the difference between different forms of a word. This can be easily achieved using spaCy, because each Token object contains an attribute named "lemma_" which contains the lemma  

![](https://i.ytimg.com/vi/pvMImQEUlN4/maxres3.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=pvMImQEUlN4&t=30) |  for the Token. So in this cell

we're going to loop over each Token in the Doc object and print out the Token and its lemma. So if I run this cell then you'll see from the output that the conjugated verbs have been returned to their base form, and the same has taken place with plural nouns, for example. Thanks for watching and I hope you found this video useful!  