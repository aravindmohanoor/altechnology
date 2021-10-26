[![#18 Processing texts efficiently using spaCy](https://i.ytimg.com/vi/00yChd449uI/maxresdefault.jpg)](https://www.youtube.com/watch?v=00yChd449uI)

## #18 Processing texts efficiently using spaCy

In this video, I'm going to show you how to process texts efficiently using spaCy 3.0.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/04_basic_nlp_continued.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=00yChd449uI&t=0) |  Hi! In this video I'm going to

show you how to process texts efficiently using the spaCy natural language processing library. When you start working with larger volumes of texts it's important to make the natural language processing pipeline as efficient as possible. What you want to do is to collect all the texts and then feed them to spaCy for processing all at once. So let's go ahead and define a toy example: so what I'm going to do here I'm going to load a small spaCy  

![](https://i.ytimg.com/vi/00yChd449uI/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=00yChd449uI&t=30) |  language model for English, assign the language model

under the variable "nlp" and then I'm going to define a list of some example sentences under the variable "sents" so now we have a toy example with three sentences, each one of them a Python string object in a list called "sents". The language model that we have stored under the variable "nlp" which is a spaCy language object contains a method named "pipe" which is optimized for processing text stored in Python lists,  

![](https://i.ytimg.com/vi/00yChd449uI/maxres2.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=00yChd449uI&t=60) |  so if we take a look at

this method we're simply going to feed the sentences to the pipe method and assign the result under the variable "docs". So if you take a look at this cell right here, I'm going to run this cell and what we get back is a generator object. In this case the generator  

![](https://i.ytimg.com/vi/00yChd449uI/maxres3.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=00yChd449uI&t=90) |  object will yield individual Doc objects, but to

examine the Doc objects we need to catch the output of the generator. To catch the output from a generator we need to cast the output into some data structure which we can then examine, and in this case the natural candidate is a list, so we use the list function from Python to cast the generator into a list and then we just replace or overwrite the variable "docs", so as you can see casting the generator into a list provides us  

#### [0:02:00](https://www.youtube.com/watch?v=00yChd449uI&t=120) |  access to the contents of the generator,

which in this case consists of three spaCy Doc objects. So just to summarize, if you use spaCy to work with large volumes of text, be sure to collect the texts into lists first and then process them using the pipe method. Thanks for watching; I hope you found this video useful and if you have any questions feel free to leave a comment below.  