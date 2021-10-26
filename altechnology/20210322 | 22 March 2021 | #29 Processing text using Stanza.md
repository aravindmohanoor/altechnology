[![#29 Processing text using Stanza](https://i.ytimg.com/vi/w8vvgP4dQTU/maxresdefault.jpg)](https://www.youtube.com/watch?v=w8vvgP4dQTU)

## #29 Processing text using Stanza

In this video, I will show you how to process text and access linguistic annotations using the Stanza natural language processing library. I exemplify this process using text written in the Wolof language.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/01_multilingual_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=w8vvgP4dQTU&t=0) |  Hi! In this video I'm going to

show you how to process texts using the Stanza natural language processing library. You can find a link to this notebook in the description below, and make sure you check out the previous video where we loaded a language model into Stanza for Wolof, which is a language spoken in West Africa. In the previous video we loaded and assigned the language model for Wolof under the variable "nlp_wo". Next we are going to feed some  

![](https://i.ytimg.com/vi/w8vvgP4dQTU/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=w8vvgP4dQTU&t=30) |  text written in Wolof as a string

object to the language model, and we store the output under the variable "doc_wo", and finally we check the type of the object that we just created by passing some text through the natural language processing pipeline. Running this cell gives us a Stanza Document object which contains all the linguistic annotations created by passing this  

#### [0:01:00](https://www.youtube.com/watch?v=w8vvgP4dQTU&t=60) |  text through the pipeline, so let's continue

by examining the Document object in greater detail, and we can start by looking at the attribute Sentences which contains all the sentences contained in the document. So under the attribute "sentences" we can find a list where each item contains a single sentence, and as usual we can use numbers in brackets to access  

![](https://i.ytimg.com/vi/w8vvgP4dQTU/maxres2.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=w8vvgP4dQTU&t=90) |  items in the list and because Python

starts counting from 0 we need to use the number 0 to access the first sentence in the list. To do so we simply run this cell. So what we find here are the linguistic annotations for individual tokens these consist of the token itself, its lemma, part of speech tags and syntactic dependencies. For some tokens you can also find information on morphology. If you're already somewhat familiar with Python you might think  

#### [0:02:00](https://www.youtube.com/watch?v=w8vvgP4dQTU&t=120) |  that the output consists of a list

with some nested dictionaries that contain the annotation, but this is actually not the case, so each sentence in this list of sentences is actually a Stanza Sentence object. If we run this cell we can check the type of the first sentence in the list of sentences and the output shows us that it's actually a Stanza Sentence object.  

![](https://i.ytimg.com/vi/w8vvgP4dQTU/maxres3.jpg)



#### [0:02:30](https://www.youtube.com/watch?v=w8vvgP4dQTU&t=150) |  If we want to get an actual

Python dictionary then we need to use the "to_dict" method of the Sentence object. We can use the "to_dict" method to create a dictionary of annotations, and in this case we're going to create a dictionary containing the annotations for the first sentence which we then store under the variable "doc_dict". After doing this we're going to get the dictionary  

#### [0:03:00](https://www.youtube.com/watch?v=w8vvgP4dQTU&t=180) |  for the first token in this sentence.

So if I run this cell what we get back is a dictionary with some keys and values, and these key and value pairs hold the linguistic annotations. We can use the keys method of a Python dictionary to get a listing of all the keys available in a dictionary and now that we have a list we can choose one of the keys and then use the key to fetch the corresponding value from the dictionary, and in this case  

#### [0:03:30](https://www.youtube.com/watch?v=w8vvgP4dQTU&t=210) |  we take the key lemma which we

provide as a string in brackets after the dictionary, which then fetches the value corresponding to this key. Thanks for watching, I hope you found this brief video on processing texts using the Stanza natural language processing library useful, and if you have any questions feel free to leave a comment below. Thanks!  