[![#14 Parsing and visualising syntactic dependencies using spaCy](https://i.ytimg.com/vi/2TBNpxAbh_g/maxresdefault.jpg)](https://www.youtube.com/watch?v=2TBNpxAbh_g)

## #14 Parsing and visualising syntactic dependencies using spaCy

In this video, I will show you how to extract information on syntactic dependencies using spaCy, and how the displacy module can be used to visualise the resulting parse trees.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/03_basic_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=0) |  Hi again! In this video I'm going

to tell you about syntactic parsing using the spaCy natural language processing library for Python. Syntactic parsing, or alternatively, dependency parsing is the task of defining syntactic dependencies that hold between Tokens. So let's start exploring syntactic parsing by looking at the dependency tags for individual Tokens. This information is available under the dep or dep_ attribute of Token objects. Once more, what we're going to do here  

#### [0:00:30](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=30) |  is we're going to loop over each

Token in the Doc object and print out the Token and its dependency tag. And if I run this cell then we will have a number of Tokens in the output together with their dependency tags. So let's take a moment to think about the role of these dependency tags. Whereas part of speech tags are associated with a single Token, these dependency tags actually  

![](https://i.ytimg.com/vi/2TBNpxAbh_g/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=60) |  indicate a relation that holds between two

Tokens. So what we're going to do here is we're going to print out the position of the Token in the Doc object, then we're going to print out the Token itself, the dependency tag and finally we're going to print out the Token that governs the current Token and its index in the Doc object. So if you take a look at this cell right here you'll  

#### [0:01:30](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=90) |  see that we again loop over the

Doc and then we print out various attributes. And as you can see you can quite flexibly combine attributes in Python as well, so in this case we print out the head and its index in the Doc object so we combine the "head" and index or "i" attributes. So let's take a moment to examine the output of this loop. What we have on the left hand side is a running  

![](https://i.ytimg.com/vi/2TBNpxAbh_g/maxres2.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=120) |  sequence of numbers which indicates the indices of

the Tokens in the Doc object, their positions and next we have the tokens themselves in the same order, followed by their dependencies, and then we have the indices of the heads that govern these Tokens and the heads themselves. And if you take a look at the first row with the index 0 you'll see that the word is the which acts as a determiner  

#### [0:02:30](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=150) |  which is governed by the second Token

the row. It's maybe a bit tricky to make sense of syntactic dependencies using output like this but luckily spaCy also provides a visualization tool to support the analysis of syntactic dependencies. So next we're going to import the "displacy" module  

#### [0:03:00](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=180) |  from spaCy that allows us to render

dependency trees. The "displacy" module has a method named "render" which takes a spaCy Doc object as its input, and if we want to draw a dependency tree we need to provide the Doc object to the render method together with two arguments. The first one is "style" because the "displacy" module can be used to draw visualizations for different  

![](https://i.ytimg.com/vi/2TBNpxAbh_g/maxres3.jpg)



#### [0:03:30](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=210) |  annotations as well. The second is "options" which

takes a Python dictionary as input and we're going to provide a key named "compact" and a value "True" to tell displacy to draw a compact tree diagram. So if I run this cell this place it will draw us a nice dependency tree that shows the dependencies between the different tokens. The syntactic dependencies are visualized using lines  

#### [0:04:00](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=240) |  which lead away from the head of

the dependency relation towards the token that's being governed by the head. These dependencies are described using a schema called Universal Dependencies and there are quite a few dependency tags, and if you don't know some of them you can ask spacY for an explanation using the "explain" function in the spaCy module. You can provide  

#### [0:04:30](https://www.youtube.com/watch?v=2TBNpxAbh_g&t=270) |  any tag as input as a string

object to this function to retrieve an explanation of the tag, so in this case we see that the tag refers to the object of a preposition. Thanks for watching and I hope you found this video useful: if you have any questions just leave a comment below.  