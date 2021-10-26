[![#19 Adding custom attributes to spaCy objects](https://i.ytimg.com/vi/oWsuCwCW29g/maxresdefault.jpg)](https://www.youtube.com/watch?v=oWsuCwCW29g)

## #19 Adding custom attributes to spaCy objects

In this video, I'm going to show you how to add custom attributes to spaCy Token, Span and Doc objects.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/04_basic_nlp_continued.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=oWsuCwCW29g&t=0) |  Hi again! In this video I'm going

to show you how to add custom attributes to various spaCy objects. You can add custom attributes to Doc, Span and Token objects in spaCy. Just to give you an example, if you're loading texts from separate files into Doc objects then it's maybe a good idea to add a custom attribute to the Doc object that points towards the source file or if you're working with transcriptions of spoken interaction you could use the attributes to add information  

#### [0:00:30](https://www.youtube.com/watch?v=oWsuCwCW29g&t=30) |  about the speaker to the spaCy span

objects. All of these custom attributes can be added using the set_extension method and what I'm going to show you next is how to add custom attributes to the Doc object, and to get started we need to import the Doc object class from the tokens submodule of spaCy. It's important to understand that now we have access to the class of Doc objects, not some  

![](https://i.ytimg.com/vi/oWsuCwCW29g/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=oWsuCwCW29g&t=60) |  individual Doc object which results from feeding some

text to a spaCy language model. So what we're going to do next is we're going to register these custom attributes using the set_extension method, so if you take a look at this cell right here, we're taking the Doc object class and using the set_extension method to register two custom attributes "age" and "location"  

#### [0:01:30](https://www.youtube.com/watch?v=oWsuCwCW29g&t=90) |  and in both cases we provide the

default argument with the value None, so by default these attributes are set to None. Python classes don't refer to any specific object, so that's why we don't have to assign these changes to the object again, but we can simply register these extensions  

![](https://i.ytimg.com/vi/oWsuCwCW29g/maxres2.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=oWsuCwCW29g&t=120) |  without doing any assignment to variable here. So

let's move forward and define a toy example, so in this case we have a dictionary with three keys, zero one and two, and under each key we have another dictionary with three keys and some values and I'm just gonna assign this dictionary into the variable "sents" dict. So what we're going to do next is we're going to loop over this dictionary. We set up a placeholder list to hold the processed text so when we get the  

#### [0:02:30](https://www.youtube.com/watch?v=oWsuCwCW29g&t=150) |  spaCy Doc objects we're going to put

them in this list right here and next we're going to loop over the dictionary using the items method which will give us both the key and the value which we assign to variables "key" and "data", so the variable data right here refers to the dictionary that contains the actual content that we want to process and store  

#### [0:03:00](https://www.youtube.com/watch?v=oWsuCwCW29g&t=180) |  so then we fetch the actual text

to be processed which is stored under the key text and feed it to the language model under "nlp" and store the result under the variable "doc". This gives us a spaCy Doc object and then we move on to assign the custom attributes "age" and "location" that we registered previously. So what we do here is we fetch the values under the keys "age" and  

![](https://i.ytimg.com/vi/oWsuCwCW29g/maxres3.jpg)



#### [0:03:30](https://www.youtube.com/watch?v=oWsuCwCW29g&t=210) |  "location" and assign them to the custom

variables "age" and "location" in the spaCy Doc object the underscore preceding the custom attributes is a kind of a fake attribute used by spaCy to separate the custom attributes from those that are native to the spaCy library. So if you assign any custom attributes you can always find them under the attribute underscore finally  

#### [0:04:00](https://www.youtube.com/watch?v=oWsuCwCW29g&t=240) |  we append the individual Doc object to

the list of Doc object under the variable "docs" so when I run this cell then we will have a list of spaCy Doc object with some custom attributes and to examine these attributes we can loop over the Doc objects in the list "docs" and print out the custom attributes, and as you can see we have the Doc itself the text and then we  

#### [0:04:30](https://www.youtube.com/watch?v=oWsuCwCW29g&t=270) |  have the custom attribute "age" and the

custom attribute "location" we can use these attributes to filter the data for further processing, so we could take for example only texts that have been written by people who are under the age of 40. Thanks for watching and I hope you found this video useful if you have any questions then just leave a comment below.  