[![#24 Examining pandas DataFrames](https://i.ytimg.com/vi/-zhW3YjhuzI/maxresdefault.jpg)](https://www.youtube.com/watch?v=-zhW3YjhuzI)

## #24 Examining pandas DataFrames

In this video, we will explore the structure of pandas DataFrames. I show you how to count unique values in a column and how to plot the result. I will also show you how to filter the data based on values.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/06_managing_data.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=0) |  Hi! In this video we're going to

examine the structure of DataFrames in pandas, which is a Python library for data analysis and management. In the previous video we loaded a CSV file into pandas and we're going to continue working with this data in this video. We assigned the data that we loaded into a DataFrame under the variable "socc" and what we're going to do first is we're going to examine all the columns in the DataFrame. And if you think about the structure of  

#### [0:00:30](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=30) |  tabular data, the columns typically give you the

types of information present in a table and in pandas if we use the columns attribute we will get a list of columns in a DataFrame. We can use brackets in pandas to access entire columns in the DataFrame and this is done by placing the name of the column in brackets as a string object after the name of  

#### [0:01:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=60) |  the dataframe. So what we're going to

do here is we fetch the column named author from the DataFrame "socc" and when I run this cell pandas returns us some output which consists of the indices for the rows and then the values contained in the column author. So what we actually have here is a pandas Series which is another type of data structure in pandas. You can think of a pandas DataFrame  

#### [0:01:30](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=90) |  consisting of multiple pandas Series which are placed

in the columns of the DataFrame so each column holds a pandas Series, and what we just retrieved from the DataFrame is then a Series object. We can easily check this by examining the type of the columns, so what I'm going to do here is I'm printing out the type of the DataFrame under the variable "socc" and then I'm going to  

![](https://i.ytimg.com/vi/-zhW3YjhuzI/maxres1.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=120) |  print out the type of the object

under "socc" in the column "author", and as you can see it is a DataFrame under the variable "socc" and then under the column "author" we have a pandas Series. And as you saw from the output, when you print out the contents of a DataFrame pandas will omit anything that comes between the first five and the last five rows, because these DataFrames can be massive.  

#### [0:02:30](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=150) |  The same applies to any output from

methods for pandas DataFrames or Series, and we can use for example the "value_counts" method to count the number of unique values in a Series, and if we now apply this to the column author to count the number of unique authors in the columns we'll see that, okay the editorial team wrote about 2 700 of the editorials – not surprisingly – and then somebody  

#### [0:03:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=180) |  named Jeffrey Simpson was also very productive

and then at the end of the result we have individuals who only contributed a single editorial. And we only see 10 values here, but if we examine the length attribute here we'll see that the DataFrame actually contains editorials from 1800  

#### [0:03:30](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=210) |  individual authors. Another very useful feature of pandas

is the ability to plot the information in Series, and what we're going to do here is we're taking the values in the author column then we're going to count the unique values in the column. We take the first 10 items in the output or in the Series and then we call the plot method and supply the argument "kind" and the value  

![](https://i.ytimg.com/vi/-zhW3YjhuzI/maxres2.jpg)



#### [0:04:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=240) |  "bar" which indicates a bar plot. and

above this line we have this piece of code saying matplotlib inline which simply tells Jupyter Notebooks to render the plot in the notebook, and as you can see what we get back is a simple bar plot of the authors containing the same information that we already examined in written form. And if you have a column or a pandas Series with numerical  

#### [0:04:30](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=270) |  values we can use the "describe" method

to get basic descriptive statistics on the data so in this case we could for example examine the number of top level comments so comments regarding the articles posted originally into the thread and then used the "describe" method to get some descriptive statistics so we'll see that we actually have um roughly 10 and 300 values and the mean value is 26,  

#### [0:05:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=300) |  so on the average the editorial got

26 top level comments. We can also filter the data according to some criteria, so if we would like to find articles or editorials with no comments at all we can use the DataFrame accessor called "loc" or location to access some rows based on their values  

#### [0:05:30](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=330) |  and we can start by looking at

the number of top level comments which are stored under the column "n_top_level_comments" , but here we need to pay a bit of attention to the syntax in pandas which is sometimes a bit confusing. So if you take a look at this cell right here so what we do first is we get the DataFrame under the variable "socc", then we call the "loc" accessor – and note the brackets here – and within the brackets we again have to refer to the DataFrame  

![](https://i.ytimg.com/vi/-zhW3YjhuzI/maxres3.jpg)



#### [0:06:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=360) |  with its name so that pandas knows

where to look for the DataFrame and the column so one needs to be very explicit. So you put the name of the DataFrame again here first and then you feed the name of the column in brackets as usual as a string object, as you can see from the quotation marks surrounding the string "n_top_ level_comments" and then outside this bracket  

#### [0:06:30](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=390) |  or after this definition of the column

in the data frame you put two equal signs which then evaluates this statement on the left against the criteria on the right, so we want to have those rows where the value of "n_top_level comments" is zero and if I run this cell what we get back is articles and as you can see we have approximately two and a half thousand articles or editorials  

#### [0:07:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=420) |  with no comments at all. We can

just double check this by looking at the value for and top level comments and as you can see they're all zero. We can also combine criteria using the & sign which is the Python operator for "and", and to do this you need to put the individual criteria in parentheses and then join them using the "and" sign so if you take a look at this cell right here  

#### [0:07:30](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=450) |  where we're looking for the first author in

the previous results of Hayden King and if the person wrote any articles with zero comments so what we do is we use the "loc" accessor again and within the brackets we put in parentheses these two statements that we want to evaluate, and here in the middle we use the and sign to combine these two criteria  

#### [0:08:00](https://www.youtube.com/watch?v=-zhW3YjhuzI&t=480) |  and if I run this cell then

we simply get one hit so there is one article written by Hayden King that received no comments at all. To summarize, pandas DataFrames consist of Series placed in columns which can be accessed and manipulated and analyzed in different ways. I hope you found this video useful and if you have any questions, just leave a comment below. Thanks!  