[![#28 Introducing Stanza: how to download language models and load them into the library](https://i.ytimg.com/vi/41aN-_NNY8g/maxresdefault.jpg)](https://www.youtube.com/watch?v=41aN-_NNY8g)

## #28 Introducing Stanza: how to download language models and load them into the library

In this video, I will introduce you to the Stanza natural language processing library for Python, and show you how to download language models for Stanza and load them into the library.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/01_multilingual_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=41aN-_NNY8g&t=0) |  Hi! In this video I'm going to

introduce you to Stanza, which is a Python library for processing many languages, and I'm also going to show you how to load a language model into Stanza for processing some texts. As usual, I already have a Notebook open and you can find a link to this Notebook in the description below. I want to start by introducing Stanza, which is a python library for processing many languages, developed by the Stanford Natural Language Processing Group.  

#### [0:00:30](https://www.youtube.com/watch?v=41aN-_NNY8g&t=30) |  The library currently provides models for over

60 languages as of 2021 which are trained on corpora annotated using the Universal Dependencies framework. This means that the models can do usual tasks such as tokenizing text into analytical units, which are then tagged for their parts of speech, morphological features, and also for their syntactic dependencies. These are the same tasks  

#### [0:01:00](https://www.youtube.com/watch?v=41aN-_NNY8g&t=60) |  that we've explored in the previous videos

using the spaCy natural language processing library. So let's start by importing the Stanza library by running this cell which contains the command "import stanza". When I run this cell this will give us access to the library. To start processing some text we need to download a language model for the language that we want to work with. This can be done using the "download" function which is available under  

#### [0:01:30](https://www.youtube.com/watch?v=41aN-_NNY8g&t=90) |  the main module "stanza", which takes a

single required argument, that is, "lang" which defines the language for which the model is downloaded. To download a model for a given language you need to provide a two-letter code to the "lang" argument as a Python string object. You can find the codes for specific language models on the Stanza website. I also provide an  

#### [0:02:00](https://www.youtube.com/watch?v=41aN-_NNY8g&t=120) |  optional argument to define where the downloaded model

should be placed but if you're happy with the default directory you don't have to provide this argument to the download function. If I run this cell Stanza will download a language model for Wolof whose language code is "wo", which is one of the many languages spoken in West Africa. Stanza will also output some information on the progress of the download. It's a good idea to check the output that stanza actually  

#### [0:02:30](https://www.youtube.com/watch?v=41aN-_NNY8g&t=150) |  finished downloading the models successfully. So what we

do now is we use the "Pipeline" class to create a natural language processing pipeline in Stanza. To create a pipeline we need to pass the argument "lang" to define the language model to be loaded into the pipeline, and optionally we can also determine the directory where we placed the downloaded language models. Then we simply assign the resulting pipeline under the variable "nlp_wo". To create the pipeline,  

#### [0:03:00](https://www.youtube.com/watch?v=41aN-_NNY8g&t=180) |  I simply run this cell which then

causes Stanza to produce some output reporting that the model was loaded successfully. So what you see on the left hand side are the processors or components of the pipeline and on the right hand side you see the packages or the corpora used to train the model,  

#### [0:03:30](https://www.youtube.com/watch?v=41aN-_NNY8g&t=210) |  so in this case all of the

components have been trained using the Wolof treebank. We can also call the pipeline object to examine the output, and as you can see the result is a Stanza Pipeline object. In the next video, I'm going to show you how to use the language model to process some text. I hope you found this short introduction to Stanza useful, and if you have any questions feel free to leave a comment below. Thanks for watching and see you soon!  