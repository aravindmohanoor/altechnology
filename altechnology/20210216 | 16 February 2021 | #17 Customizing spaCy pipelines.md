[![#17 Customizing spaCy pipelines](https://i.ytimg.com/vi/F4SJJQF49b0/maxresdefault.jpg)](https://www.youtube.com/watch?v=F4SJJQF49b0)

## #17 Customizing spaCy pipelines

In this video, I'm going to show you how to inspect and customize natural language processing pipelines in spaCy 3.0.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/04_basic_nlp_continued.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=F4SJJQF49b0&t=0) |  Hi! In this video I'm going to

show you how to inspect and customize a natural language processing pipeline in spaCy. As usual you can find a link to this notebook in the description below. Let's start by inspecting the language object in spaCy which contains the natural language processing pipeline. So first I'm going to load a small language model for English and assign the resulting language object under the variable "nlp"  

![](https://i.ytimg.com/vi/F4SJJQF49b0/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=F4SJJQF49b0&t=30) |  and then I'm going to call the

variable "nlp" to check out the result, and what we get is a language object that contains a language model for the English language. Let's take a closer look under the hood, so what's actually contained in this language object. We can do so by using the pipeline attribute of a language object. If I call the pipeline attribute we will get a list of tuples, to be more precise, this is a SimpleFrozenList object from spaCy  

#### [0:01:00](https://www.youtube.com/watch?v=F4SJJQF49b0&t=60) |  which consists of tuples that have two

items in each tuple. The first item in the tuple is the name of the component and the second one refers to the actual object doing the processing, the component itself, and these are the components that perform the actual tasks when providing text as input to a spaCy language model. You should see quite a few familiar names already in this list,  

![](https://i.ytimg.com/vi/F4SJJQF49b0/maxres2.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=F4SJJQF49b0&t=90) |  so we have a tagger, we have

a parser, and we have a component for named entity recognition, for example. It's important to keep in mind that all of these components come with a computational cost, so if you're doing some processing then you might want to consider what are actually the tasks that you need to do, so if you don't need named entity recognition then just leave the component  

#### [0:02:00](https://www.youtube.com/watch?v=F4SJJQF49b0&t=120) |  out to speed up the processing. So

if you don't need the output of some component then one should exclude it from the pipeline. The easiest way to achieve this is to actually exclude some of the components when loading the model, so in this cell right here what we're doing is we're loading a spaCy language model, a small model for English, but we also pass the "exclude" argument which takes a list as an input, as you can see from the brackets, which contains the names  

![](https://i.ytimg.com/vi/F4SJJQF49b0/maxres3.jpg)



#### [0:02:30](https://www.youtube.com/watch?v=F4SJJQF49b0&t=150) |  of the components that should not be

loaded when initializing the model. So here we are loading the model again and overwriting the previous one that we had stored under the variable "nlp", but this time we exclude both named entity recognition and the parser components. So if I run this cell and then we examine the pipeline you'll see that the parser and the named entity recognition components  

#### [0:03:00](https://www.youtube.com/watch?v=F4SJJQF49b0&t=180) |  are gone. Some components may depend on

the output of another component so it's always a good idea to use the analyze_pipes() method available for the language object to check that there are no errors. By providing the argument "pretty" to the analyze_pipes() method and setting its value to True you will get a nice output and an overview of the various components. spaCy will also tell you if any potential problems are found; what you also get is a useful summary of all the components and  

#### [0:03:30](https://www.youtube.com/watch?v=F4SJJQF49b0&t=210) |  the annotations that they assign to various

spaCy Doc, Span and Token objects. Thanks for watching and I hope you found this video useful. If you have any questions just leave a comment below!  