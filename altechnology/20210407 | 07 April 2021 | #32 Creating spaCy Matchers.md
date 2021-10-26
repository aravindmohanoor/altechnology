[![#32 Creating spaCy Matchers](https://i.ytimg.com/vi/aVPMzk2rCP4/maxresdefault.jpg)](https://www.youtube.com/watch?v=aVPMzk2rCP4)

## #32 Creating spaCy Matchers

In this video, I will show you how to create spaCy Matcher objects for matching linguistic patterns.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/02_pattern_matching.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=aVPMzk2rCP4&t=0) |  Hi! In this video I'm going to

introduce you to Matchers in the spaCy natural language processing library, and how these Matchers can be used to search linguistic annotations for structural patterns. spaCy provides three types of Matchers: the first type is called a Matcher, which can be used to match Tokens or their sequences based on their attributes, such as part of speech tags. Second type is a DependencyMatcher which can be used to search for patterns  

![](https://i.ytimg.com/vi/aVPMzk2rCP4/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=aVPMzk2rCP4&t=30) |  among syntactic dependencies, and the third one

is a PhraseMatcher, which can be used to match spaCy Doc objects to spaCy Doc objects. If you want to use any type of spaCy Matcher you first need to load a language model for the language that you're trying to match. So what I'm going to do here is I import the spaCy library and then load a small language model for English. Now that we have  

![](https://i.ytimg.com/vi/aVPMzk2rCP4/maxres2.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=aVPMzk2rCP4&t=60) |  loaded a language model we can proceed

to import the Matcher class which is available under the sub module in spaCy. This gives us access to the Matcher class, so we can now create Matcher objects. In this case I'm simply going to create a basic Matcher by calling the Matcher class and then providing the vocabulary of the language model as input to the "vocab" argument of the  

![](https://i.ytimg.com/vi/aVPMzk2rCP4/maxres3.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=aVPMzk2rCP4&t=90) |  Matcher class, and then I assign the

resulting Matcher object under the variable Matcher. Now if I run this cell we'll also call the variable to examine the output and we see that indeed this created a spaCy Matcher object. The same procedure applies to every type of Matcher in spaCy, so to create a Matcher you need to provide the vocabulary of the language model to the Matcher.  

#### [0:02:00](https://www.youtube.com/watch?v=aVPMzk2rCP4&t=120) |  In the following videos I'm going to

show you how to define pattern rules for matching various types of linguistic structures using these spaCy Matcher classes. I hope you found this short video useful and if you have any questions, feel free to leave a comment below. Thanks for watching!  