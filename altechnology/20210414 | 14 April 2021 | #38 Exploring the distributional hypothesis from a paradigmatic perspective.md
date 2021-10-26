[![#38 Exploring the distributional hypothesis from a paradigmatic perspective](https://i.ytimg.com/vi/Zh600gBfn4o/maxresdefault.jpg)](https://www.youtube.com/watch?v=Zh600gBfn4o)

## #38 Exploring the distributional hypothesis from a paradigmatic perspective

In this video, we will examine the distributional hypothesis from a paradigmatic perspective, that is, how we can characterise a word by observing the words that co-occur with the word.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_iii/03_embeddings.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Natural Language Processing for Linguists playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0LQ_6gz2cCksbLhE1PfX4R



#### [0:00:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=0) |  Hi! In this video we will explore the

distributional hypothesis from a paradigmatic perspective. This means that we focus on individual words and the words that tend to co-occur with them. Just to give you a recap: the distributional hypothesis proposed by Zellig Harris states that similarity in meaning results in similarity of distribution and by distribution Harris refers to the contexts in which a given linguistic unit  

#### [0:00:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=30) |  such as a word occurs. What the

paradigmatic perspective refers to in this case is that we focus on individual words or lemmas in this case rather than looking at their distribution across some units of analysis, such as a clause, as we did in the previous video. To put it simply, we try to characterize individual lemmas numerically by capturing information about  

#### [0:01:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=60) |  the contexts in which they occur. We'll

start by getting the unique lemmas from the DataFrame that we created in the previous video by using the columns attribute of the DataFrame and its tolist() method to get a list of unique lemmas in our example data. This gives us a list  

#### [0:01:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=90) |  of 23 string objects that give the

unique lemmas in our vocabulary. To set us up for tracking the co-occurrences of these lemmas, we will create a new pandas DataFrame and use the list of lemmas for both the index, that is, the rows, and the columns. We then fill each cell in the DataFrame  

![](https://i.ytimg.com/vi/Zh600gBfn4o/maxres1.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=120) |  with the value 0 using the fillna()

method. This gives us a DataFrame with the same categories across the columns and the rows with values of 0 in each cell. We can think of this empty DataFrame as a beginning of a co-occurrence matrix, which can be used to track how many times a given lemma  

#### [0:02:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=150) |  occurs within some distance of another lemma.

So what we want to do is to fill this DataFrame with information about co-occurrences of lemmas to make this easier. We will start by combining all of the spaCy Doc objects that we have currently under a list named "docs" into a single Doc object. This can be achieved by importing the Doc object from the tokens submodule of spaCy  

#### [0:03:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=180) |  and then creating a new Doc object

and using the from_docs() method to create a combined Doc object. This method takes a list of Doc objects as its input and returns a single Doc object which we assign under the variable "combined_docs" to track the co-occurrences of words. Let's assume that the two preceding or following words on either side of the word constitute its neighbors and this is  

#### [0:03:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=210) |  the information that we want to capture

in our DataFrame. To do this, we can use the nbor() or neighbour method of a spaCy Token. This method takes a number as its input, which determines the position of the neighbor relative to the current Token, so for example we could give the value -1 to the neighbor method to get the previous Token. The problem is that not all of the  

#### [0:04:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=240) |  Tokens have neighbours, so we need to

take this into account in our code when we look for co-occurring lemmas. We start by looping over the Tokens in the spaCy Doc object named "combined_docs". We then define a nested for loop that is a for loop within a for loop that loops over a list with four numbers these numbers refer to the neighboring Tokens, so for example,  

![](https://i.ytimg.com/vi/Zh600gBfn4o/maxres2.jpg)



#### [0:04:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=270) |  as I said previously, -1 would indicate

the previous Token. We then use the "try" statement to attempt to run the following code block under the "try" statement. So what we do here is we take the neighbors of the Token one by one by looping over the positions and storing their lemma under  

#### [0:05:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=300) |  the variable "neighbour_lemma". We then store this information

in the DataFrame using the "add" accessor which uses brackets to access a specific cell of the DataFrame, so in this case we take the lemma of the Token that we're currently processing during the loop over the "combined_docs" Doc  

#### [0:05:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=330) |  object, and then we take the current

neighboring lemma and increment the value of this cell by one using the plus and equal sign. So just to recap, for every Token we loop over the four positions, and try to observe the neighboring lemmas and add this information to the DataFrame. However, if the token that we're looping over doesn't have neighbors which raises an index error,  

#### [0:06:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=360) |  we use the except statement to avoid

an error and simply instruct Python to move on to the next position. This collects the co-occurrence counts for each lemma within two lemmas on either side into the DataFrame, and we can now examine the result by calling the variable "lemma_df". This gives us the co-occurrence counts for each lemma and we can see for example that the lemmas Tallinn  

#### [0:06:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=390) |  and Helsinki co-occur within two words of

another twice in the data. Note that in this DataFrame we have the same information in the columns and the rows. We can think of the information that we've collected into the columns and the rows for each lemma as a vector that describes the context in  

![](https://i.ytimg.com/vi/Zh600gBfn4o/maxres3.jpg)



#### [0:07:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=420) |  which the lemma occurs. In other words,

we use the counts to encode information about the collocated words, and this of course takes us back to the quip by J.R. Firth about the way you can know a word by the company it keeps. We can also relate this to the distributional hypothesis, as we would expect paradigmatic alternatives, that is, lemmas with similar meanings that can be used roughly  

#### [0:07:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=450) |  interchangeably to have similar distributions in terms of

the contexts in which these lemmas occur. Because we now have numerical representations in the form of 23-dimensional vectors for each lemma, we can use cosine similarity as introduced in the previous video to measure the distance between these vectors. So in this cell we get the vectors with the co-occurrence counts  

#### [0:08:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=480) |  for the words or lemmas "Tallinn" and

"Helsinki" and compare their cosine similarity. Note that we have to wrap these vectors into brackets for input to the cosine_similarity() function from scikit-learn. This gives us a value of 0.42 which might suggest some similarity between the vectors  

#### [0:08:30](https://www.youtube.com/watch?v=Zh600gBfn4o&t=510) |  as 1.0 would indicate perfect similarity, but of

course here we have a set of data that is quite limited with just 23 lemmas, but still this suggests that the lemmas "Tallinn" and "Helsinki" occur in similar contexts, which we know to be true from the example that we examined in the previous video. Of course we could refine these representations by observing more data,  

#### [0:09:00](https://www.youtube.com/watch?v=Zh600gBfn4o&t=540) |  thus having a more complete picture of

the context in which these words occur, but the problem again is that by increasing the size of the vocabulary we would also have to increase the dimensionality of the embedding space. Thanks for watching, I hope you found this video useful and if you have any questions about the distributional hypothesis feel free to leave a comment below. Thanks!  