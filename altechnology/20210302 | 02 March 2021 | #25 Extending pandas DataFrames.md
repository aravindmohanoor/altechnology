[![#25 Extending pandas DataFrames](https://i.ytimg.com/vi/Yj87Gy28vqs/maxresdefault.jpg)](https://www.youtube.com/watch?v=Yj87Gy28vqs)

## #25 Extending pandas DataFrames

In this video, I will show you how to add new information to pandas DataFrames by processing the existing data. We use pandas to perform calculations and spaCy to manipulate textual data. 



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/06_managing_data.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=0) |  Hi again! In this video I'm going

to show you how to add information to pandas DataFrames. We're going to continue to work with the data that we loaded into pandas in the previous videos, so under the variable "socc" we have a pandas DataFrame that contains some editorials and articles from a Canadian newspaper. So what we're going to do next is we're going to add some new columns into the pandas DataFrame imagine that we want to calculate the ratio of top level comments  

#### [0:00:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=30) |  and the discussions below them. So what we're

going to do is we're going to add a column named "comments_ratio" to the DataFrame "socc" and how we're going to do this is we're going to take the DataFrameadd the name of the new column in brackets after the name of the variable and then we use a single equal sign to assign the value None to each  

#### [0:01:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=60) |  row in this column, and when I

run this cell the column gets created and we can easily check this by using the "head" method to retrieve the first five rows in the DataFrame so if you take a look right here you can see an empty column here on the right hand side with the name "comments_ratio" so let's go ahead and fill this column with some values and to do so we can move down  

#### [0:01:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=90) |  and then again assign some values into

the column in the DataFrame as done in this cell right here. So we call the DataFrame, then we specify the column and then we use the equal sign and then we have a reference to the column containing the number of top level comments divided by the values in the column for all the comments,  

#### [0:02:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=120) |  and if I run this cell the

column for the comments ratio gets populated by the result of this calculation. Moving ahead, if you remember from the previous videos some of the articles didn't get any comments at all, so in this case we would be dividing zero by zero. So if we filter the DataFrame for articles with no top level comments and look at the first five examples then if we scroll to the right and look at the "comments_ratio" then what we see is  

![](https://i.ytimg.com/vi/Yj87Gy28vqs/maxres1.jpg)



#### [0:02:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=150) |  a NaN value here instead of the

original None that we created when creating the placeholder column and NaN simply means not a number and this is simply because you cannot divide by zero. pandas automatically ignores these NaN values when performing calculations on the column values,  

#### [0:03:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=180) |  so if we use the "describe" method

for example to get some descriptive statistics for the "comments_ratio" column. If I run this cell you can see that the count is only approximately 7700, although we have nearly eleven thousand articles in this DataFrame. This means that only these seven thousand eight hundred items were included in the calculation. Just as easily we can do some  

#### [0:03:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=210) |  natural language processing and store the results into

the pandas DataFrame, so we could just start by taking the articles with a high number of top level comments, as expressed by the comments ratio, and also filter the data for those articles that actually received more than 200 comments. So this is what we do in this cell right here, so if you take a look we have a combined  

#### [0:04:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=240) |  criteria – so two different criteria for

filtering the DataFrame as introduced in the previous video – and now we're simply going to take the first five values of the DataFrame using the "head" method, and as you can see we have some articles here with quite some few comments and what we're going to do next is we're going to import spaCy and then we're going to load a medium-sized language model for the English language, which we're going to use to  

#### [0:04:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=270) |  process the titles of these articles. And

now we're going to create an empty placeholder column for the titles that we're going to feed to the spaCy language model, so we're going to continue by fetching each title of the article which is stored in the column "title", and then we feed it to the language model stored under the variable "nlp" for processing, and then we store the output  

![](https://i.ytimg.com/vi/Yj87Gy28vqs/maxres2.jpg)



#### [0:05:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=300) |  into a column named "processed_title". And to do

this we're going to use the apply "method", and this is super easy. As the name of the "apply" method suggests, it simply takes whatever is provided to the "apply" method and applies it to the contents of the column, so going through each row in the column and applying whatever we provide to the "apply" method. To put it simply, we get the string objects from the title column and provide them to the language model under  

#### [0:05:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=330) |  the variable "nlp". So let's go ahead

and run this cell: what we get back is the processed titles here in the column on the right hand side, and if we scroll further down, we can examine some of the individual rows in the column "processed_title" and we're going to use the "at" accessor to access the processed title column add the row with the index 2, and what we get back is  

#### [0:06:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=360) |  the name of the article and if

we check its type it's actually a spaCy Doc object. Next we're going to do something a bit more complicated, so we're going to define our own Python function to fetch lemmas for each noun in the processed titles. So if you take a look at this cell right here  

#### [0:06:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=390) |  we're going to define the function by

starting with the command "def" which stands for define, which is then followed by the name that we give to the function, which in this case is "get_ nouns" and after the name of the function we define all the inputs that need to be provided to the function, and in this case we define a single input and we refer to this input  

#### [0:07:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=420) |  using the variable named "nlp_text" and then

we finish the define or def command with a colon. And as you can see, the definition that comes afterwards needs to be indented and we're going to start by the command "assert" and what this command does is it evaluates a statement on the left hand side of the two equal signs: we have this statement that the type of the  

![](https://i.ytimg.com/vi/Yj87Gy28vqs/maxres3.jpg)



#### [0:07:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=450) |  object fed to this function has to

be the object type that we define here on the right hand side, so a spaCy Doc object. This ensures that we will get an error if we try to provide – let's say Python string objects to our function. Next we create an empty list named "lemmas" that we then populate by looping over the "nlp_text", which is a spaCy Doc object, and we examine  

#### [0:08:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=480) |  each token. We take the "tag_" attribute and

look for nouns, and in this case you know the fine grained part of speech tag for a noun is two capital Ns, so NN, and if we find a match in the spaCy Doc object, we add the lemma of the token to the list named  

#### [0:08:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=510) |  lemmas. When we have looped over the

spaCy Doc object, we return this list of lemmas. So this is the output of the function so the input to the function is a spaCy Doc object and the output is a Python list containing the lemmas as string objects, and to define the function to make it available in Python we simply run this cell and now we have the "get_nouns" function available in Python. And what we're going to do next is we're going to apply this function to titles in the  

#### [0:09:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=540) |  column "processed_title". So in this case we're simply

going to assign the output – that is the list of lemmas – into the column nouns, as defined here on the left hand side of the equal sign, and as you can see we don't even have to create a placeholder column we can just assign directly data to the pandas DataFrame and then on the right hand side we're going to take the spaCy Doc object  

#### [0:09:30](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=570) |  in the column "processed_title". And then we call

the "apply" method and then we provide the name of our function that we just defined, so if we examine the output on the right hand side we have now a column named "nouns" which contains a list of lemmas that we just extracted from the spaCy Doc objects in the column "processed_title". Thanks for watching;  

#### [0:10:00](https://www.youtube.com/watch?v=Yj87Gy28vqs&t=600) |  I hope you found this video useful

and if you have any questions just leave a comment below. Thanks!  