[![#31 Interfacing the spaCy and Stanza libraries using spacy-stanza](https://i.ytimg.com/vi/Yqy7I7c7EXc/maxresdefault.jpg)](https://www.youtube.com/watch?v=Yqy7I7c7EXc)

## #31 Interfacing the spaCy and Stanza libraries using spacy-stanza

In this video, I will show you how to use Stanza language models in the spaCy natural language processing library.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/01_multilingual_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=Yqy7I7c7EXc&t=0) |  Hi! In this video I'm going to

show you how to interface the Stanza and spaCy natural language processing libraries using a third library named spacy-stanza. spacy-stanza is a small library developed by the developers of spaCy, which allows you to use Stanza language models in spaCy. There is, howeve,r one limitation to what can be done, that is, the language in question must be supported by both Stanza and spaCy. For example, we cannot use the  

![](https://i.ytimg.com/vi/Yqy7I7c7EXc/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=Yqy7I7c7EXc&t=30) |  Stanza language model for Wolof that we've

been exploring in the previous videos in spaCy, because spaCy does not support Wolof. To get started, let's import the spaCy and spacy-stanza libraries, and note that the name of the spacy-stanza module contains an underscore, not a dash. By importing these libraries we now have access to them in Python, so what we're going to do next is we use  

#### [0:01:00](https://www.youtube.com/watch?v=Yqy7I7c7EXc&t=60) |  the load_pipeline function from the spacy-stanza module to

load a Stanza pipeline for the Finnish language. We then assign the result under the variable "nlp_fi". The load pipeline function requires at least one argument named "name", which defines the code for the language for which the language model will be loaded, and also optionally if you've stored the Stanza models  

![](https://i.ytimg.com/vi/Yqy7I7c7EXc/maxres2.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=Yqy7I7c7EXc&t=90) |  in some directory other than the default

one, then you also need to use the "dir" argument to point out where the Stanza models can be found. So let's just load the model, and as you can see, you get the typical output produced by Stanza, so you have the various components of the natural language processing pipeline and the data or corpora used to train those components, which in this case correspond to the Turku Dependency Treebank, and then we can  

#### [0:02:00](https://www.youtube.com/watch?v=Yqy7I7c7EXc&t=120) |  just continue by examining the output, so

what did we get by calling the load pipeline function. And if we run this cell then we see that oh it's a spaCy language object for Finnish. So what we got back was a spaCy language object which contains a pipeline for processing text written in the Finnish language and this language object contains the same functionalities  

![](https://i.ytimg.com/vi/Yqy7I7c7EXc/maxres3.jpg)



#### [0:02:30](https://www.youtube.com/watch?v=Yqy7I7c7EXc&t=150) |  as the language objects that we learned to

use in part two of these materials. We can, for example, take some text in Finnishg and then provide it as a string object to the spaCy language model under "nlp_fi" and then what we get back is a spaCy Doc object, so we can for example get the sentences contained in this document using the "sents" attribute and  

#### [0:03:00](https://www.youtube.com/watch?v=Yqy7I7c7EXc&t=180) |  cast the output into a list, and

this will give us then the sentences contained in this document. I hope you found this short video useful, and if you have any questions about interfacing the Stanza and spaCy libraries using spacy-stanza, then feel free to leave a comment below. Thanks!  