[![#15 Sentence segmentation using spaCy](https://i.ytimg.com/vi/NknDZSRBT7Y/maxresdefault.jpg)](https://www.youtube.com/watch?v=NknDZSRBT7Y)

## #15 Sentence segmentation using spaCy

In this video, I will show you how to do sentence segmentation using spaCy, which refers to the task of splitting longer texts into sentences.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/03_basic_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=NknDZSRBT7Y&t=0) |  Hi again! In this video I'm going

to talk about sentence segmentation using spaCy. So far we've been talking about the Doc object in spaCy as a container for texts and their linguistic annotations. Just what qualifies as an appropriate text for the Doc object depends on the use case: if you're dealing with let's say some old newspaper articles that come in separate text files then maybe you should assign each of those text files into its own Doc object.  

![](https://i.ytimg.com/vi/NknDZSRBT7Y/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=NknDZSRBT7Y&t=30) |  The same applies if you would be

dealing let's say with customer emails or feedback. One of the best ways to impose some structure on larger texts is to perform sentence segmentation which is the task of splitting longer texts into sentences. You can access the results of sentence segmentation in spaCy using the attribute "sents" of a Doc object. So let's loop over the sentences  

![](https://i.ytimg.com/vi/NknDZSRBT7Y/maxres2.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=NknDZSRBT7Y&t=60) |  contained in the Doc object under the

variable Doc and count them at the same time using Python's "enumerate" function. This function returns a count that increases with each item in the loop, so what we do here is we loop over the Doc object and its attribute "sents" which we wrap into the "enumerate" function and this gives us two items that we need to position after the "for"  

![](https://i.ytimg.com/vi/NknDZSRBT7Y/maxres3.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=NknDZSRBT7Y&t=90) |  statement. The first variable number refers to the

count coming from the "enumerate" function and the second variable "sent" refers to the sentence returned by the sents attribute. We then simply print out the number and the sentence returned from the sent attribute. So if I run this cell we'll see that this Doc object contains a single sentence. I  

#### [0:02:00](https://www.youtube.com/watch?v=NknDZSRBT7Y&t=120) |  hope you found this video useful, and

if you have any questions just leave a comment below.  