[![#23 Loading data into pandas DataFrames](https://i.ytimg.com/vi/UQYyCVGZbvk/maxresdefault.jpg)](https://www.youtube.com/watch?v=UQYyCVGZbvk)

## #23 Loading data into pandas DataFrames

In this video, I show you how to load a CSV file into pandas, a Python library for manipulating and analysing data.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/06_managing_data.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=0) |  Hi! In this video I'm going to

show you how to load data into pandas, which is a Python library for managing and manipulating data. As usual, you can find a link to this notebook in the description below. To get started, we need to import the pandas library, and as usual we're going to do this using the import command, but this time we're going to import the library using an alias for the name so that we don't always have to write the name of the library when we're referring to it. So if you look at this cell where we import the pandas library,  

#### [0:00:30](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=30) |  you can see that the import pandas

command is followed by the statement "as" and then two letters pd, which is now the abbreviation that we used to refer to the pandas library. And now that I've imported the library we can access all its functions using the abbreviation "pd". Now that we've imported the library we can move ahead and load some data into pandas,  

![](https://i.ytimg.com/vi/UQYyCVGZbvk/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=60) |  and in this case we're going to

load a single CSV file which stands for comma separated values. It's a common format for storing tabular data and in this case, we are going to load a part of a corpus called the SFU Opinion and Comments Corpus which contains opinion articles from the Globe and Mail which is a Canadian newspaper. So we have this file named soccgnmarticles.csv  

#### [0:01:30](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=90) |  in a directory named data, as indicated

in this cell, and we're going to use the "read_csv" function from pandas to read the comma separated values file and then we're going to assign the result under the variable "socc". And when I run this cell what we get back is a pandas DataFrame which is a pandas specific object for storing tabular data. And we can examine  

![](https://i.ytimg.com/vi/UQYyCVGZbvk/maxres2.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=120) |  the output the type of the object,

and as you can see it's indeed a DataFrame. The DataFrame contains a wealth of methods for exploring its contents and just to give you an idea of a couple of these methods, we're going to use the "head" method to print out the first five rows of the DataFrame under the variable "socc". And now that I run this cell we'll get the first five rows in the DataFrame. The DataFrame has several columns, and as you can  

#### [0:02:30](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=150) |  see from the headers we have things

like article id, its title, address, the author, when it was published, and the number of comments and then the article text itself all in their own columns. And what we have here in the rows are first the number of the rows, the so-called indices, and as you can see the counting starts from zero as usual in Python. So here we have the first five  

![](https://i.ytimg.com/vi/UQYyCVGZbvk/maxres3.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=180) |  rows, and this is essentially data in

a tabular format, and because the data is in a tabular format we can of course access values stored in specific cells defined by the columns and the rows and one way to do this is to use the "at" accessor to inspect single items stored in a DataFrame. So how this works is that we're going to call the "at" accessor and then – note the brackets – we're  

#### [0:03:30](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=210) |  going to put the index first. In

this case we're going to fetch the title of the article at index 123. We first put in the row index and then we give the name of the column as a string object. In the next few videos we're going to take a look at how to manipulate data using pandas I  

#### [0:04:00](https://www.youtube.com/watch?v=UQYyCVGZbvk&t=240) |  hope you found this video useful and

if you have any questions just leave a comment below. Thanks!  