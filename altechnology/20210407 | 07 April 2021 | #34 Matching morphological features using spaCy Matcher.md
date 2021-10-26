[![#34 Matching morphological features using spaCy Matcher](https://i.ytimg.com/vi/9WbONZ8iJlc/maxresdefault.jpg)](https://www.youtube.com/watch?v=9WbONZ8iJlc)

## #34 Matching morphological features using spaCy Matcher

In this video, I will show you how to define strict and flexible pattern rules for matching morphological features using the spaCy Matcher class.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/02_pattern_matching.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=0) |  Hi! In this video I'm going to

show you how you can use spaCy Matchers to search for specific morphological features. As you may remember from previous videos, spaCy stores the results of morphological analysis under the attribute "morph" of a Token object, and in some cases these morphological analyses can be very rich and in some other cases they can consist of one or two attributes only. In all cases the attributes are represented using string  

#### [0:00:30](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=30) |  objects, where the different morphological features are separated

by a vertical bar. The actual features then are defined using the equal sign. So let's create a new spaCy Matcher object for matching morphological features, and as usual we provide the vocabulary of the language model to the Matcher object when we  

#### [0:01:00](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=60) |  create the Matcher. So let's define a

pattern rule for two tokens. For the first token we want to match fine-grained part-of-speech tags that have the value "NNP" which stands for proper noun and we also add the operator plus so that these proper nouns can occur more than one time if necessary. This allows us then to catch, for example, combinations of first and last names.  

![](https://i.ytimg.com/vi/9WbONZ8iJlc/maxres1.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=90) |  For the second Token we want to

match coarse part-of-speech tags that have the value "verb" and which also have all of the following morphological features, so their number has to be singular; they have to be in the third person; they have to be of the present tense; and they have to have a finite form, so we're being very strict here and we provide this sequence of morphological features  

#### [0:02:00](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=120) |  using the same pattern that spaCy uses for

the morphological analysis. As usual both of these patterns are defined using Python dictionaries which we then add into a Python list to be added to the "morph" Matcher. To add the pattern to the Matcher we use the "add" method and provide the name of the pattern as a string object followed by the list to the  

#### [0:02:30](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=150) |  argument "patterns", which is wrapped into square brackets

because the input has to be a list of lists as explained in the previous video, and then we also provide the argument "greedy" with the value "longest". This causes the Matcher to look for matches in a greedy way, so it looks for the longest matching sequence before returning any result, and this is  

![](https://i.ytimg.com/vi/9WbONZ8iJlc/maxres2.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=180) |  especially important if you use operators such

as plus, which then allow a Token to be matched one or more times. So what we're going to do now is we add the pattern to the Matcher and then match the Doc object that we've already stored under the variable "doc" and then loop over the results, and as you can see we only get a few matches because the criteria that we defined were quite strict.  

#### [0:03:30](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=210) |  So the next question is how to

loosen the criteria to match just some of the morphological features to define a more flexible pattern. We still have to use the "morph" key for the dictionary, but instead of defining a string object with some morphological features, we provide a dictionary with the key "IS _SUPERSET". So let's unpack this a bit: so how does the is superset  

#### [0:04:00](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=240) |  pattern work? So we can think of

the morphological features associated with a given token as a set, so for example in the previous case the set could consist of the following four items, so number, person, tense and verb form, and each of these of course have their specific values. If we would have another set with just one item such as Tense=Present, so for the present tense,  

#### [0:04:30](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=270) |  then we could describe the relationship between these

two sets by stating that the first set which contains four items is a superset of the second set which has only one item. So this is how the is superset keyword works, so spaCy retrieves the morphological features for a given Token and then examines whether these features are a superset of the features defined  

![](https://i.ytimg.com/vi/9WbONZ8iJlc/maxres3.jpg)



#### [0:05:00](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=300) |  in the search pattern in the Matcher

object. So just to recap you need to provide a dictionary under the key "morph" when defining a pattern for a Token which then consists of a dictionary with the key "IS_SUPERSET" whose value is a list of string objects, and each string object needs to match a morphological feature as defined  

#### [0:05:30](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=330) |  in the universal dependencies formalism, so in this

case we're simply going to match verbs in a past tense, so we provide a list with a single item that is the string object Tense=Past. Then we add the pattern to the Matcher under the name "past_tense" and then we apply the Matcher  

#### [0:06:00](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=360) |  to the Doc object under the variable

"doc", and finally we store the results under the variable "morph_results". So if we loop over the results and print out the name of the pattern, then the matching sequence and the morphological information for the final token in the sequence, that is, the verb, then we see that all of the verbs have the morphological attribute Tense=Past.  

#### [0:06:30](https://www.youtube.com/watch?v=9WbONZ8iJlc&t=390) |  So in this video you learned to

match morphological features using spaCy Matchers and how to match the patterns strictly and more flexibly, and if you have any questions about defining morphological patterns then feel free to leave a comment below. Thanks for watching!  