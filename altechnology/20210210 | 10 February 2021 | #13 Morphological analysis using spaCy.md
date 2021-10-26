[![#13 Morphological analysis using spaCy](https://i.ytimg.com/vi/1iliKkbHF30/maxresdefault.jpg)](https://www.youtube.com/watch?v=1iliKkbHF30)

## #13 Morphological analysis using spaCy

In this video, I will show how you can extract morphological information from words using the spaCy 3.0 natural language processing library.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/03_basic_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=1iliKkbHF30&t=0) |  Hi again! In this video I'm going

to show you how to extract morphological information from texts processed using the spaCy library. Morphemes are the smallest meaningful units in a language, and there are two types of morphemes. Free morphemes which can stand on their own and bound morphemes which attach to other morphemes. So these morphemes shape the external form of a word and these particular forms are then associated with particular grammatical  

![](https://i.ytimg.com/vi/1iliKkbHF30/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=1iliKkbHF30&t=30) |  functions. Just to give you an example

from the English language, you can use a bound morpheme "s" and attach it to the end of a noun to create a plural form. spaCy performs morphological analysis automatically and stores the result under the attribute called "morph" for every Token object. So in this cell we're looping over each Token in the Doc object and then we print out each Token  

#### [0:01:00](https://www.youtube.com/watch?v=1iliKkbHF30&t=60) |  and its morphological information. So as you can

see from the output most tokens contain morphological information. To retrieve morphological information in a programmatic way, we must use the "get" method available for the morph attribute. So the "get" method takes a Python string as input and in this case we want to get the aspect of the 23rd Token in the Doc  

![](https://i.ytimg.com/vi/1iliKkbHF30/maxres2.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=1iliKkbHF30&t=90) |  object. So if I run this cell

space it will return us morphological information in a list, as you can see from the surrounding brackets, and this list contains a single item "perf" which refers to the perfective aspect. So what you want to do in most cases is to retrieve all the morphological information available and this can be achieved very easily using the "to_dict" method  

#### [0:02:00](https://www.youtube.com/watch?v=1iliKkbHF30&t=120) |  which converts the output into a dictionary. A

dictionary is a Python data structure that consists of key and value pairs. Python dictionaries are marked using curly brackets, and each key and value pair is separated by a colon. These pairs, in turn, are separated by commas. So let's just use the "to_dict" method to retrieve morphological information for  

![](https://i.ytimg.com/vi/1iliKkbHF30/maxres3.jpg)



#### [0:02:30](https://www.youtube.com/watch?v=1iliKkbHF30&t=150) |  this Token, and as you can see

we have three different key/value pairs in this dictionary: one for mood, one for tense, and one for verb form. You can use the key to retrieve the corresponding value from a Python dictionary. So what I'm going to do here is I'm assigning the dictionary that contains the morphological information under the variable "morph_dict"  

#### [0:03:00](https://www.youtube.com/watch?v=1iliKkbHF30&t=180) |  and I'm then placing the key mood

as a string within brackets right after the dictionary name to retrieve the value for this key. And what we get in this case is indicative or "ind". To sum it up, morphological information imposes a lot of structure on free text and you definitely should learn how to leverage this information for structuring and  

#### [0:03:30](https://www.youtube.com/watch?v=1iliKkbHF30&t=210) |  exploring your data. Thanks for watching; I

hope you found this video useful and see you soon.  