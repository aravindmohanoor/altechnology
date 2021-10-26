[![#37 Exploring the distributional hypothesis from a syntagmatic perspective](https://i.ytimg.com/vi/zwtvIomLJSw/maxresdefault.jpg)](https://www.youtube.com/watch?v=zwtvIomLJSw)

## #37 Exploring the distributional hypothesis from a syntagmatic perspective

In this video, we will examine the distributional hypothesis from a syntagmatic perspective, that is, how we can characterise a piece of text by observing the words that occur within that piece.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/03_embeddings.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=0) |  Hi! In this video we will explore the

distributional hypothesis from a syntagmatic perspective. To do this, we need to start by defining units of analysis in which we look for co-occurring words. The scope of the analytical units can be motivated linguistically, so they can consist of clauses or sentences, for example, or they can just consist of some arbitrary units of analysis in which we look for  

#### [0:00:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=30) |  co-occurring words. To get started, let's import the

spaCy natural language processing library and load a medium-sized language model for the English language. We then define a toy example of five clauses in a list that we assign under the variable "examples". Next we feed the examples to the language model using the pipe() method and cast the output into a list.  

#### [0:01:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=60) |  This gives us a list of spaCy

Doc objects to describe the words that co-occur within a single clause or a spaCy Doc object. We first need to come up with a way of describing the vocabulary for all of the Doc objects. For convenience, we're simply going to work with lemmas instead of the inflected forms of the words. To count the unique lemmas across all Doc objects in our toy example,  

#### [0:01:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=90) |  we start by importing the lemma object

from the "attrs" submodule of spaCy. We then use a Python dictionary comprehension to loop over the list of spaCy Doc objects while counting them using Python's enumerate() function, which gives us two items for each loop.  

#### [0:02:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=120) |  The variable "i" refers to the count

whereas the variable "doc" refers to the Doc object. On the left hand side of the "for" statement we call the count_by() method of the Doc object and feed the attribute "lemma" to this method. We store the number or the count of the Doc object as the key  

![](https://i.ytimg.com/vi/zwtvIomLJSw/maxres1.jpg)



#### [0:02:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=150) |  of the resulting dictionary, whereas the value consists

of the output from the count_by() method. This gives us a dictionary that counts the unique lemmas in each spaCy Doc object in the list. If you're wondering about the weird sequences of numbers, these are simply spaCy Lexeme objects that refer to entries in the language model's vocabulary. What we do in this cell right here is we map the Lexeme objects to their human readable forms and store these under the  

#### [0:03:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=180) |  variable "lemma_counts", so essentially updating the dictionary. To

make sense of these counts, we import the pandas library and convert the dictionary into a pandas DataFrame which was introduced in the previous videos. Essentially, we want to compile all of the information  

#### [0:03:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=210) |  about the unique lemmas into a tabular

form in a pandas DataFrame. What we do here is we import the pandas library and then we create a new DataFrame object by calling the DataFrame class from the pandas library and we then use the from_dict() method from the DataFrame class to which we give  

#### [0:04:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=240) |  our dictionary of limit counts. We then

sort the index in an ascending order. We assign the resulting DataFrame under the variable "df" which we then fill using zeros for those cells that don't have any values. Finally, we flip the DataFrame on its side using the transpose method, or the attribute capital T. This gives us a DataFrame in which the rows stand for the  

#### [0:04:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=270) |  individual Doc objects or clauses, whereas the columns

give unique lemmas in the vocabulary across all the Doc objects. So we have five rows for our five clauses and 23 columns one for each unique lemma, so for example on the first row the lemmas "Finland" and "Helsinki" occur both once in the Doc object. We can think of the information stored for each Doc object  

![](https://i.ytimg.com/vi/zwtvIomLJSw/maxres2.jpg)



#### [0:05:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=300) |  in the rows of the DataFrame as

a vector, that is, a list of numbers that encodes information about co-occurring words. So what we have here on the first row of the DataFrame at index 0 is a 23 dimensional vector. The dimensions of the vector correspond to the number of  

#### [0:05:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=330) |  unique lemmas in the vocabulary. From the perspective

of the distributional hypothesis, we can now think of this vector as encoding information about co-occurring selections made within the vocabulary. We can use the values attribute of a DataFrame object under the variable "df" to retrieve a vector for each row in the DataFrame, so now that the  

#### [0:06:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=360) |  syntagmatic structure of each Doc object is represented

numerically using a vector, that is, we have an idea about the distribution of lemmas within each Doc. We can start using these vectors and all of the mathematical operations available for manipulating vectors to explore our data. Although it's difficult to imagine, each of these vectors represents a  

#### [0:06:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=390) |  point in a 23-dimensional space and one

thing that we can do to compare these points in the 23-dimensional space is to calculate their cosine similarity. You can think of cosine similarity as a measure of how close the two points are to each other in the high dimensional space. What we're going to do next is we import a measure of cosine similarity from the scikit-learn library  

#### [0:07:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=420) |  and we then calculate cosine similarity between the

values stored in the DataFrame and we store the calculation under the variable "sim". This gives us a five by five matrix in which each cell gives the cosine similarity value between two Doc objects in our example data, and as I said above,  

#### [0:07:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=450) |  this value tells you how close the

two vectors are in the high dimensional space. To help us make sense of these values we can import the heatmap() function from the seaborn visualization library and render a heat map of these values what we get back is a heat map in which the rows and the columns stand for the individual Doc objects in our example, whereas the colors are mapped to  

![](https://i.ytimg.com/vi/zwtvIomLJSw/maxres3.jpg)



#### [0:08:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=480) |  values of cosine similarity on the right,

and as you can see there is a diagonal line across the table showing values of 1.0 which is entirely normal because the vector for every Doc object is naturally compared to itself as well. Of course, if you compare the cosine similarity  

#### [0:08:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=510) |  of identical vectors the result will be

1.0 indicating perfect similarity. If you take a look at the Doc objects at indices 0 and 1, so if you look at the row for 1 and then the column for 0, you see that these two examples have high cosine similarity, and according to the distributional hypothesis, because these two vectors have similar distributions of values, which is why they are  

#### [0:09:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=540) |  close to each other in the high

dimensional space, they should also be semantically similar. So let's explore this by getting the examples from the list of Doc objects under "docs" at index zero and one, so here we have two examples "Helsinki is the capital of Finland" and "Tallinn is the capital of Estonia", as you can see both of these examples feature a similar syntagmatic structure, that is,  

#### [0:09:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=570) |  "is the capital of", and this illustrates

how we can use vectors to describe syntagmatic structures essentially using counting the unique lemmas as an abstraction mechanism for encoding linguistic choices into a numerical form. There are a few problems to this approach, however, for example,  

#### [0:10:00](https://www.youtube.com/watch?v=zwtvIomLJSw&t=600) |  every time we would add another word

to our vocabulary then we would have to increase the dimensionality of the vector or embedding space to accommodate this new addition to the vocabulary. We also don't have any information on in which sequence these limits or items in the vocabulary  

#### [0:10:30](https://www.youtube.com/watch?v=zwtvIomLJSw&t=630) |  occur. Thanks for watching; I hope you

found this video useful, and if you have any questions about the distributional hypothesis, feel free to leave a comment below. Thanks!  