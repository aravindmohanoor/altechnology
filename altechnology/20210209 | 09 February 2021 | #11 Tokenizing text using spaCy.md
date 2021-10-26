[![#11 Tokenizing text using spaCy](https://i.ytimg.com/vi/hVOSVlWnl_k/maxresdefault.jpg)](https://www.youtube.com/watch?v=hVOSVlWnl_k)

## #11 Tokenizing text using spaCy

In this video, I will tell you about tokenization in the spaCy 3.0 natural language processing library for Python.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/03_basic_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=hVOSVlWnl_k&t=0) |  Hi! In this video we're going to

talk about tokenization, which is a fundamental step in any natural language processing pipeline. As usual, you can find a link to this notebook in the description below. Tokenization refers to the process of breaking text down into analytical units that are in need of further processing. Keep in mind that computers treat text as a sequence of characters, not words. Thus we need to find the units  

![](https://i.ytimg.com/vi/hVOSVlWnl_k/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=hVOSVlWnl_k&t=30) |  that are actually in need of further

linguistic processing. For written texts in languages such as English where the words are separated by empty spaces, tokenization may appear as a trivial task, but this is not the case for languages such as Japanese or Chinese where you don't have empty space separating the words. So if you take a look at this diagram right here, you'll see what happens to text when it's fed to a language model in spaCy. So first of all the text gets tokenized  

![](https://i.ytimg.com/vi/hVOSVlWnl_k/maxres2.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=hVOSVlWnl_k&t=60) |  before applying any of the further processing steps.

The Doc object is essentially a sequence of Token objects in spaCy, which store the results of various natural language processing tasks that we'll encounter in the upcoming videos. Let's take a look at the Doc object stored under the variable "doc", and what we're going to do here is we're going to loop over the Tokens in the Doc object  

![](https://i.ytimg.com/vi/hVOSVlWnl_k/maxres3.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=hVOSVlWnl_k&t=90) |  and print out each Token. And as

you can see, the output shows that the words and punctuation marks constitute separate tokens. In the following videos, we're going to look at some of the linguistic annotations that have been created when this text was passed through the language model and how they can be accessed through the spaCy Token objects. Thanks for watching;  

#### [0:02:00](https://www.youtube.com/watch?v=hVOSVlWnl_k&t=120) |  I hope you found this video useful

and if you have any questions just leave a comment below.  