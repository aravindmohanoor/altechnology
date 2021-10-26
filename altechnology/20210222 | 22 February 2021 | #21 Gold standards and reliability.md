[![#21 Gold standards and reliability](https://i.ytimg.com/vi/eBJDxHUxRwc/maxresdefault.jpg)](https://www.youtube.com/watch?v=eBJDxHUxRwc)

## #21 Gold standards and reliability

In this video, I discuss the notion of a gold standard and its role in evaluating the performance of natural language processing models. Because a gold standard should be reliable, I show you how to measure agreement between annotators using Cohen's kappa, a measure of inter-annotator agreement implemented in the scikit-learn library.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/05_evaluating_nlp.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=0) |  Hi! In this video I'm going to

tell you about the concept of a gold standard and what this concept means in the context of natural language processing. A gold standard or a ground truth refers to some body of human verified data that can be used as a benchmark for evaluating the performance of natural language processing models. To put it simply, a gold standard is a baseline for human performance on some natural language processing task. It's also important to understand  

#### [0:00:30](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=30) |  that gold standards are abstractions of language use.

Think for example of placing words into specific word classes: those classes are not given to us by nature, but they are abstractions imposed on language by theories of grammar. Language is naturally subjective and ambiguous, so we might not always agree on how to describe a particular instance of language use. Generally we want to  

![](https://i.ytimg.com/vi/eBJDxHUxRwc/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=60) |  have reliable gold standards that we agree

on in order to have a solid benchmark for measuring the performance of natural language processing models. We can measure agreement between individuals on some body of data using statistical methods known as inter-annotator agreement measures. One traditional measure of agreement is known as Cohen's kappa, which ranges from -1 to plus one where -1 indicates perfect disagreement on the data,  

#### [0:01:30](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=90) |  whereas one stands for complete agreement. Zero, in

turn, indicates completely random agreement between the two individuals. Cohen's kappa is limited to just two annotators or two individuals describing the data and the categories in which the data is placed must be defined in advance. In  

![](https://i.ytimg.com/vi/eBJDxHUxRwc/maxres2.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=120) |  other words, we want to correct the

estimate for the possibility that the individuals describing the data just happen to agree by chance. We can calculate Cohen's kappa using Python by using the scikit-learn library: in this cell I import the cohen_kappa_score function from the scikit-learn library and more specifically it's sub-module for metrics. When I run this cell  

#### [0:02:30](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=150) |  then we will have the cohen_kappa_score function available

in Python. Next I'm going to define a toy example which consists of two Python lists that contain five part of speech tags each and I assign them under the variables "a1" and "a2". Now that we've defined the two lists which do not contain the same items so they don't completely agree with one another, we're going to feed the two lists to the cohen_kappa_score function that we just imported from scikit-learn  

![](https://i.ytimg.com/vi/eBJDxHUxRwc/maxres3.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=180) |  and this is simply done by inputting

both of the variables referring to these lists to the cohen_kappa_score function and placing them within the parentheses, and if I run this cell then we will get a Cohen's kappa score value of 0.44. So this is our estimate of agreement which has been corrected for the chance that the two annotators represented by these lists  

#### [0:03:30](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=210) |  would agree by chance. Finally we can

take a look at the table proposed by Landis and Koch which gives some criteria on making sense of the Cohen kappa score values and in this case our result 0.44 would indicate moderate agreement. To sum it up, if you're developing a gold standard for some tasks it's rarely feasible to have all of the data annotated by two or more  

#### [0:04:00](https://www.youtube.com/watch?v=eBJDxHUxRwc&t=240) |  individuals. In most cases you take a

subset of the data and measure agreement on this subset. I hope you found this video useful and if you have any questions just leave a comment below.  