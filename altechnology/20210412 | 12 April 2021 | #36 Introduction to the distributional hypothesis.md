[![#36 Introduction to the distributional hypothesis](https://i.ytimg.com/vi/ZB28symH8Mg/maxresdefault.jpg)](https://www.youtube.com/watch?v=ZB28symH8Mg)

## #36 Introduction to the distributional hypothesis

In this video, I will introduce you to the distributional hypothesis, which underlies word embeddings, a key technique in modern natural language processing.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/03_embeddings.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=ZB28symH8Mg&t=0) |  Hi! In this video I will introduce you

to the distributional hypothesis, which underlies word embeddings a key technique in modern natural language processing. Word embeddings are a technique that allows learning numerical representations that approximate the meaning of words. The quote "You shall know a word by the company it keeps" by the English linguist John Rupert Firth has often been described as the inspiration  

#### [0:00:30](https://www.youtube.com/watch?v=ZB28symH8Mg&t=30) |  for the technique of word embeddings. What

Firth means by this quote is that the meaning of a word can be inferred by examining the word in its context of occurrence. According to Firth, meaning emerges from the complex interplay of phonetics, grammar, lexicography and semantics in some context or situation in which language is used. This of course is a fairly broad take  

![](https://i.ytimg.com/vi/ZB28symH8Mg/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=ZB28symH8Mg&t=60) |  on context, which emphasizes the role of

the situation in which language is used. A more extreme version of the relationship between a word and its immediate context can be found in the distributional hypothesis put forward by Zellig Harris in 1954. The distributional hypothesis proposes that linguistic elements such as words can be characterized by their  

#### [0:01:30](https://www.youtube.com/watch?v=ZB28symH8Mg&t=90) |  distribution in the linguistic system. What the term

distribution refers to in this context is the way words tend to co-occur with each other. It's important to understand that the distribution of words in a language is not random, but can be characterized using probabilities, and some words are more likely to co-occur with one another than some others. The core idea behind the distributional hypothesis has been recently summarized by Gemma Boleda as "similarity in  

![](https://i.ytimg.com/vi/ZB28symH8Mg/maxres2.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=ZB28symH8Mg&t=120) |  meaning results in similarity of linguistic distribution". Just

to give you an example, if you were given a verb such as "enjoy" you could probably come up with some words that could be more or less likely to occur in connection with this word, and if you came up with some context in which the verb could be used, such as "I enjoy running", then you can probably also come up with  

#### [0:02:30](https://www.youtube.com/watch?v=ZB28symH8Mg&t=150) |  a way of replacing the verb "enjoy"

without changing the meaning of the utterance too much. You could, for example, replace the verb enjoy with the verb "like" as in "I like running", and this is because according to the distributional hypothesis, these verbs can be used interchangeably, because they occur in similar contexts. Magnus Sahlgren has argued that the distributional hypothesis has its roots in structuralist soil,  

![](https://i.ytimg.com/vi/ZB28symH8Mg/maxres3.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=ZB28symH8Mg&t=180) |  meaning Ferdinand de Saussure's ideas about the structure

of language. De Saussure famously described the structure of language from two perspectives: langue, which is the abstract system constituted by language itself, and parole, the particular instances of language produced by the underlying system of langue.  

#### [0:03:30](https://www.youtube.com/watch?v=ZB28symH8Mg&t=210) |  Saussure also described langue as having paradigmatic and

syntagmatic axes of organization. The paradigmatic organization allows making choices among alternatives, whereas the syntagmatic organization allows taking selections made among paradigmatic alternatives and combining them into larger units. In the following videos, we will explore the distributional hypothesis from both paradigmatic and syntagmatic perspectives, while seeking to  

#### [0:04:00](https://www.youtube.com/watch?v=ZB28symH8Mg&t=240) |  quantify information about the occurrence of linguistic units

on both axes of organization. Thanks for watching, I hope you found this brief introduction to the distributional hypothesis useful, and if you have any questions, feel free to leave a comment below! Thanks!  