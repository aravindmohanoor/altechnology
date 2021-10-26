[![#33 Defining pattern rules for spaCy Matcher](https://i.ytimg.com/vi/YT7GMDjPlrw/maxresdefault.jpg)](https://www.youtube.com/watch?v=YT7GMDjPlrw)

## #33 Defining pattern rules for spaCy Matcher

In this video, I will show you how to define pattern rules for spaCy Matcher objects, which allow you to match linguistic patterns. We also explore the use of operators for making the rules more flexible.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/02_pattern_matching.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=0) |  Hi! In this video I'm going to

show you how to define rules for matching linguistic patterns using the spaCy Matcher class. In this case we already have a spacCy Matcher object created as instructed in the previous video by loading a language model and providing its vocabulary to the Matcher object, and now we're ready to define a pattern rule for matching linguistic structures in some body of annotated text. The pattern rules for spaCy Matcher are  

#### [0:00:30](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=30) |  defined using Python lists and dictionaries, so in

order to define a rule that matches several Tokens we need to create a list first and then populate this list with dictionaries, so that each dictionary stands for a single Token. So in this case we're going to define a pattern that looks for pronouns and verbs that follow them, and to do so, we define a list with two  

#### [0:01:00](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=60) |  dictionaries. In both cases the dictionary key consists

of the string "POS" in capital letters which stands for part of speech, and then the values correspond to the particular word classes that we want to match, so pronoun and verb. So these dictionaries constitute the list items which are separated with a comma as usual, whereas the key and value pairs in the dictionaries are  

![](https://i.ytimg.com/vi/YT7GMDjPlrw/maxres1.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=90) |  separated by a colon. To add this

rule to the Matcher that we've already created we need to use the "add" method which takes two inputs. The first one is a name for the pattern which is just used to distinguish between multiple patterns, because a single Matcher can hold several patterns, and the second argument is named "patterns" which takes a list of lists  

#### [0:02:00](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=120) |  as input, so if you're wondering why

we wrap the list under the variable "pronoun_verb" again in square brackets for input to the "patterns" argument, this is simply because we need to provide a list of lists, because this allows the matcher to contain several pattern rules under the same identifier or name for the pattern. To use the Matcher and the pattern that it now contains  

#### [0:02:30](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=150) |  to search some text we simply feed

a spaCy Doc object to the Matcher object, and in this case we also provide the argument "as_spans" with the value "True" to the Matcher object so that we get back spaCy Spans, that is continuous sequences of Token objects from the Doc that match our pattern,  

![](https://i.ytimg.com/vi/YT7GMDjPlrw/maxres2.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=180) |  and then we store the result under

the variable "result". And if I run this cell what we get back is a list of spaCy Spans matching our pattern, so if we examine the first item in the list under the index 0 we see that it consists of the pronoun it and the verb aimed, and we also have some very useful attributes for this sequence, such as start and end which give  

#### [0:03:30](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=210) |  you the indices of these Tokens in

the Doc object. You also have a label under the attribute label which gives you this weird sequence of numbers. This weird sequence of numbers is actually a spaCy Lexeme object which corresponds to an entry in the language model's vocabulary and we can use this lexeme to index the vocabulary as shown in this cell right here, and to fetch the text  

#### [0:04:00](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=240) |  attribute for this Lexeme, which gives us

the name of the pattern that we defined for the pattern that we added to the Matcher. This is useful for distinguishing between multiple patterns contained in a single Matcher object. spaCy pattern rules can be made more flexible by using operators which are added to the dictionaries that correspond to individual Tokens  

![](https://i.ytimg.com/vi/YT7GMDjPlrw/maxres3.jpg)



#### [0:04:30](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=270) |  under the key "op". To illustrate the

use of operators, let's add another token into the pattern that we defined before and use the operator "+" to allow this Token to occur one or more times. So what we do here is we define another list named "pronoun_aux_verb"  

#### [0:05:00](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=300) |  which consists of a list with three

dictionaries, and in the middle dictionary which stands for the auxiliary between the pronoun and the verb we also have the operator under the key "op" which has the value plus indicating that this Token – an auxiliary – can occur one or more times, and then we simply add this rule to the Matcher under the name "pronoun+aux+verb" and then we search the  

#### [0:05:30](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=330) |  Doc object under the variable "doc" for

matches and request the results to be returned as Spans. If we loop over the results and print out the name of the pattern and the sequence that matches the pattern that is the spaCy Span object, then we'll see that this Matcher now can match pronouns and auxiliaries and verbs regardless of how many auxiliaries  

#### [0:06:00](https://www.youtube.com/watch?v=YT7GMDjPlrw&t=360) |  there are between the pronoun and the

verb, and this is due to having the operator plus included in the pattern rule. Thanks for watching, I hope you found this video useful, and if you have any questions about spaCy Matchers, then feel free to leave a comment below. Thanks!  