[![#9 Loading a language model into spaCy](https://i.ytimg.com/vi/hJ6PJoITa6I/maxresdefault.jpg)](https://www.youtube.com/watch?v=hJ6PJoITa6I)

## #9 Loading a language model into spaCy

In this video, I will show how to load a language model into the spaCy 3.0 natural language processing library for Python.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/03_basic_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=hJ6PJoITa6I&t=0) |  Hi! In this video I'm going to

show you how to load a language model into the spaCy natural language processing library for Python. You can find a link to this notebook in the description below. spaCy is a natural language processing library for Python which can be used to perform various kinds of natural language processing tasks, such as tagging parsing and sentence segmentation, for example. But to do any of this spaCy requires a language model that has been trained to perform these tasks. Before we get started,  

![](https://i.ytimg.com/vi/hJ6PJoITa6I/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=hJ6PJoITa6I&t=30) |  we need to import spaCy into Python, and

as usual we use the import command and the name of the library, so if we run this cell then we will have spaCy available in Python. And since no error was raised we can assume that spaCy was imported successfully. So now that we have imported the spaCy library we can move on to loading a language model. spaCy  

![](https://i.ytimg.com/vi/hJ6PJoITa6I/maxres2.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=hJ6PJoITa6I&t=60) |  provides pre-trained language models for several languages, which

means that these models have been trained to perform some basic natural language processing tasks. And what we're going to do next is we're going to load a small language model for English into spaCy, and in this cell right here we call the "load" function from the spaCy library and provide a string object referring to the small  

![](https://i.ytimg.com/vi/hJ6PJoITa6I/maxres3.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=hJ6PJoITa6I&t=90) |  language model to the function as input,

and then we assign the resulting language model under the variable "nlp". Now if I run this cell, the model gets loaded and if we call the variable "nlp" we'll see that the result is a spaCy language object that contains a language model for the English language. The language object is essentially a pipeline that uses the language  

#### [0:02:00](https://www.youtube.com/watch?v=hJ6PJoITa6I&t=120) |  model that we just loaded to perform

the natural language processing tasks it has been trained to do. The following videos will show you how to apply the language model to some actual texts. I hope you found this video useful, and if you have any questions just leave a comment below.  