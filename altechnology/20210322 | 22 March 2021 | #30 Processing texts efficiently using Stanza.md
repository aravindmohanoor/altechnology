[![#30 Processing texts efficiently using Stanza](https://i.ytimg.com/vi/L2MmfJ3x5Jk/maxresdefault.jpg)](https://www.youtube.com/watch?v=L2MmfJ3x5Jk)

## #30 Processing texts efficiently using Stanza

In this video, I will show you how to process texts efficiently in batches using the Stanza natural language processing library. I exemplify the process using texts written in the Wolof language.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/01_multilingual_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=0) |  Hi! In this video I'm going to

show you how to efficiently process multiple texts using the Stanza natural language processing library. As usual I already have a notebook open, and you can find a link to this notebook in the description below. Make sure you also watch the previous videos where we loaded a Stanza language model for the Wolof language. If you need to process multiple documents using Stanza what you want to do first is to collect all the documents  

#### [0:00:30](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=30) |  into a Python list. In this case

I'm simply going to define a toy example consisting of a couple of documents written in the Wolof language, which I then assign under the variable "str_docs". Next we are going to use a Python list comprehension to loop over the list of documents which are stored as string objects and we then cast them into Stanza document objects  

![](https://i.ytimg.com/vi/L2MmfJ3x5Jk/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=60) |  and prepare them for the linguistic annotation as

a part of the natural language processing pipeline. If you're unfamiliar with list comprehensions in python make sure you check out the notebook for a step-by-step explanation. Just to walk you through this step right here: we loop over the list of string objects stored under the variable "str_docs" and we refer to each item or document in the list using the variable "doc",  

#### [0:01:30](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=90) |  and then on the left hand side

of the for statement we create a Stanza Document object which takes two inputs. The first one is an empty list which will contain the linguistic annotations and the second one is an argument named "text" to which we then feed the item referred to using the variable "doc" and this results in a Python list consisting of Stanza document objects, which we  

![](https://i.ytimg.com/vi/L2MmfJ3x5Jk/maxres2.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=120) |  store under the variable "docs_wo_in" meaning the input

documents to the natural language processing pipeline. If I run this cell what we get back is something that seems to be two empty Python lists within a single list, but don't let this output fool you, because these are actually Stanza Document objects that lack any linguistic annotations. We can easily check this by using the  

#### [0:02:30](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=150) |  "type" function in Python and to check

the type of the first object in this list which indeed is a Stanza document object. We can use the "text" attribute of a Stanza document object to check that our input texts actually made it into the Document, and as you can see from the output the input text is stored under the attribute "text" so the Document has been created successfully,  

![](https://i.ytimg.com/vi/L2MmfJ3x5Jk/maxres3.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=180) |  but it hasn't been annotated for its

linguistic features yet. So at this stage we have a list of Stanza document objects without any linguistic annotations, and what we're going to do next is we feed this list of Document objects to the language model for annotation, and to do this we're going to use the language model that we created in the previous video and feed the variable "docs_wo_in"  

#### [0:03:30](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=210) |  to the language model which we have stored

under the variable "nlp_wo", and then we store the result in a different variable. So instead of passing a single Python string to the language model for annotation, we pass a list of Document objects and the output then is a list of document objects with linguistic annotations. So if we call the variable that we just created to check the output we'll see that indeed these documents have been now  

#### [0:04:00](https://www.youtube.com/watch?v=L2MmfJ3x5Jk&t=240) |  populated with linguistic annotations. So just to summarize,

when working with multiple documents it's a good idea to collect the Documents into a list and feed them all at once to the language model for efficient processing. Thanks for watching, I hope you found this video useful, and if you have any questions feel free to leave a comment below.  