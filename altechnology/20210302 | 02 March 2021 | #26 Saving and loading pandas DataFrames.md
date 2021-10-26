[![#26 Saving and loading pandas DataFrames](https://i.ytimg.com/vi/yK_3QgOVXIo/maxresdefault.jpg)](https://www.youtube.com/watch?v=yK_3QgOVXIo)

## #26 Saving and loading pandas DataFrames

In this video, I will show you how to write pandas DataFrames to disk and how to load them back into Python.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/06_managing_data.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



![](https://i.ytimg.com/vi/yK_3QgOVXIo/maxres1.jpg)



#### [0:00:00](https://www.youtube.com/watch?v=yK_3QgOVXIo&t=0) |  Hi! In this video I'm going to

show you how to write a pandas DataFrame to disk and how to load it again into Python. The easiest way to write a pandas DataFrame to disk is to use the "to_pickle" method. The "to_pickle" method takes a string as input which defines a path to the file into which the DataFrame should be written. In this case we already have a pandas DataFrame under the variable "df", and what we're going to do is we're simply going to use the "to_pickle" method to write the  

![](https://i.ytimg.com/vi/yK_3QgOVXIo/maxres2.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=yK_3QgOVXIo&t=30) |  DataFrame to disk to the directory data

into a file named pickled_df.pkl. So running this cell causes the DataFrame to be written to disk and we can easily check whether the data actually made it to the file on disk by reading the file again, and this can be done using the "read_pickle" method. So what we're going to do is we're using the "read_pickle" method  

![](https://i.ytimg.com/vi/yK_3QgOVXIo/maxres3.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=yK_3QgOVXIo&t=60) |  from pandas and assign the result to

the variable named "df_2". So by running this cell we read the pickled DataFrame and what we see is actually the DataFrame that we just wrote on disk, and we can easily verify that these are the same two DataFrames by comparing the data frames using two equal signs. So if I run this cell then pandas will perform  

#### [0:01:30](https://www.youtube.com/watch?v=yK_3QgOVXIo&t=90) |  a comparison cell by cell and returns

the value True if the value is the same in each DataFrame, and as you can see all cells have the value True. Thanks for watching, I hope you found this short video useful, and if you have any questions feel free to leave a comment below.  