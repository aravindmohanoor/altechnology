[![#10 Providing text as input to a spaCy language model](https://i.ytimg.com/vi/kJjKJ6qlQmM/maxresdefault.jpg)](https://www.youtube.com/watch?v=kJjKJ6qlQmM)

## #10 Providing text as input to a spaCy language model

In this video, I will show how to provide text as input to a language model in the spaCy 3.0 natural language processing library.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/03_basic_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



![](https://i.ytimg.com/vi/kJjKJ6qlQmM/maxres1.jpg)



#### [0:00:00](https://www.youtube.com/watch?v=kJjKJ6qlQmM&t=0) |  Hi! In this video I'm going to

show you how to provide text as input to a language model in spaCy. You can find a link to this notebook in the description below. So at this stage we've already loaded a language model into spaCy as shown in the previous video, and what we're going to do next is we're going to define a simple example text stored into a Python string object, and here we simply assign this sentence from an  

![](https://i.ytimg.com/vi/kJjKJ6qlQmM/maxres2.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=kJjKJ6qlQmM&t=30) |  old newspaper article into a string object

under the variable "text", and then we call the variable to look at its contents. So we can now refer to this string object using the variable "text", and what we're going to do next is we're going to feed this variable to the spaCy language model stored under the variable "nlp". This is just like using a Python function,  

![](https://i.ytimg.com/vi/kJjKJ6qlQmM/maxres3.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=kJjKJ6qlQmM&t=60) |  so we place the variable "text" within

the parentheses here, and then we take the output and store the result under the variable "doc", and this variable name already alludes to a specific type of object in spaCy called a Doc object which is a container for text and its annotations. So if we examine the Doc object under the variable "doc" then we'll see that this contains the text  

#### [0:01:30](https://www.youtube.com/watch?v=kJjKJ6qlQmM&t=90) |  that we originally assigned under the variable "text".

In the following videos we're going to take a look at what actually happened under the hood when we provided the text as input to the language model under the variable "nlp". I hope you found this video useful and be sure to check out the following videos on how to use the language model in practice.  