[![#35 Matching syntactic dependencies using spaCy DependencyMatcher](https://i.ytimg.com/vi/gUbMI52bIMY/maxresdefault.jpg)](https://www.youtube.com/watch?v=gUbMI52bIMY)

## #35 Matching syntactic dependencies using spaCy DependencyMatcher

In this video, I will show you how to define pattern rules for spaCy DependencyMatcher objects, which allow you to match patterns among syntactic dependencies.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/02_pattern_matching.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=gUbMI52bIMY&t=0) |  Hi! In this video I'm going to

show you how to match syntactic dependencies using the spaCy DependencyMatcher. If you want to use spaCy to match syntactic dependencies between Token objects, you need to use the DependencyMatcher class. This class is available under the Matcher submodule of spaCy, and as usual, to create a DependencyMatcher object, you need to provide the vocabulary of a language model as input to  

#### [0:00:30](https://www.youtube.com/watch?v=gUbMI52bIMY&t=30) |  the DependencyMatcher object. So what I'm going to

do here is create a DependencyMatcher and store the result under the variable "dep_matcher". This provides us with a DependencyMatcher that's now ready to store the pattern rules for matching syntactic dependencies. Defining pattern rules  

#### [0:01:00](https://www.youtube.com/watch?v=gUbMI52bIMY&t=60) |  for syntactic dependencies is a bit different than

matching – let's say – part of speech tags. You need to start by defining an anchor pattern on which the entire rule is built. For example, if we want to match verbs and their nominal subjects in the syntactic structure, we should take the verb as the anchor pattern. To define this pattern, we use a Python dictionary as usual,  

![](https://i.ytimg.com/vi/gUbMI52bIMY/maxres1.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=gUbMI52bIMY&t=90) |  and we have to provide values for

two keys: "RIGHT_ID" and "RIGHT_ATTRS" or attributes. The "RIGHT_ID" key holds a name for the pattern provided as a string object that can be referred to by subsequent patterns on the right hand side of this pattern rule. The "RIGHT_ATTRS" holds the  

#### [0:02:00](https://www.youtube.com/watch?v=gUbMI52bIMY&t=120) |  linguistic features of the anchor token, so

in this case we simply determine that the anchor should have verb as its coarse part of speech tag. So this dictionary gives us the pattern for a single token that matches the verb in the pattern that we're building up. You can think of  

#### [0:02:30](https://www.youtube.com/watch?v=gUbMI52bIMY&t=150) |  the rule for matching syntactic dependencies as a

kind of a chain, and what we just did is define the first link in the chain, which is now on the left hand side, and to the right we start building new chains that contain some criteria to be matched. So what we're going to do next is we determine a pattern for the next link in this chain to the right hand side of the anchor,  

#### [0:03:00](https://www.youtube.com/watch?v=gUbMI52bIMY&t=180) |  and we start by providing the key

"LEFT_ID" which again takes a value as a string object that refers to the name of the pattern on the left hand side of the current pattern. As you may remember we have the pattern for the verb on the left hand side as the anchor, so we need to provide the name of that pattern here under the key "LEFT_ID". Next, we use the key "REL_OP"  

![](https://i.ytimg.com/vi/gUbMI52bIMY/maxres2.jpg)



#### [0:03:30](https://www.youtube.com/watch?v=gUbMI52bIMY&t=210) |  to define a relation operator which determines the

relationship between the current pattern and that referred to using the key "LEFT_ID". So the greater than symbol defines that the pattern stored under "LEFT_ID", that is, the anchor, should be the head of the current pattern. Next,  

#### [0:04:00](https://www.youtube.com/watch?v=gUbMI52bIMY&t=240) |  we use the "RIGHT_ID" key to define

a name for this pattern, in case we want to extend this chain and define another pattern on the right hand side of this link, and then we use the "RIGHT_ATTRS" key to define the syntactic dependency that holds between this current pattern  

#### [0:04:30](https://www.youtube.com/watch?v=gUbMI52bIMY&t=270) |  and the pattern defined using the "LEFT_ID". Then

we simply add these dictionaries into a list named "def_pattern" that we can add to the DependencyMatcher. As usual, then we apply the Matcher to the Doc object under the variable "doc" and store the matches  

![](https://i.ytimg.com/vi/gUbMI52bIMY/maxres3.jpg)



#### [0:05:00](https://www.youtube.com/watch?v=gUbMI52bIMY&t=300) |  under the variable "dep_matches". What we get back

is a Python list consisting of tuples, as marked by the parentheses, which contains two items a spaCy Lexeme object that refers to the name of the pattern that we just gave to this pattern to be matched, so "nsubj_verb" and then a Python list consisting of indices in the Doc object that match our query. So  

#### [0:05:30](https://www.youtube.com/watch?v=gUbMI52bIMY&t=330) |  what we're going to do next is

we're going to loop over these matches and we unpack the tuple, so that we take the first item in the tuple and assign it under the variable "pattern_name" and then we take the second part that is the list of indices in the Doc object and store that under the variable "matches". We then take the list containing the matches  

#### [0:06:00](https://www.youtube.com/watch?v=gUbMI52bIMY&t=360) |  and assign the items in this list

to the variables "verb" and "subject". Finally, we use the Lexeme object stored under the variable "pattern_name" to fetch the name of the pattern from the vocabulary of the spaCy Language object, and then we print out a tabulator character to separate the output and then we slice the Doc object for the subject and the verb, and separate these two  

#### [0:06:30](https://www.youtube.com/watch?v=gUbMI52bIMY&t=390) |  by a sequence of three full stops,

and what we get back is the name of the pattern that we added to the DependencyMatcher and then the matching pattern consisting of the subject and then the verb. Thanks for watching, I hope you found this video useful, and if you have any questions about using the spaCy DependencyMatcher, feel free to leave a comment below. Thanks!  