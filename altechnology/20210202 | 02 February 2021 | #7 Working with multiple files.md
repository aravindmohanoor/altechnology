[![#7 Working with multiple files](https://i.ytimg.com/vi/UYyqQD3w59c/maxresdefault.jpg)](https://www.youtube.com/watch?v=UYyqQD3w59c)

## #7 Working with multiple files

In this video, we will use the Path class from Python's pathlib module to retrieve and open multiple files stored in a directory.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/02_basic_text_processing_continued.html#Processing-multiple-files



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=UYyqQD3w59c&t=0) |  Hi! In this video I'm going to

show you how to efficiently manipulate multiple files using Python. As usual, you can find a link to this notebook in the description below. Quite often when working with text your data might be spread out over various files and you need to open all these files, perform some operations save the results and then you want to close the files and do all of this programmatically. This is fairly easy to achieve using the Path class from Python module called "pathlib". So what we're going to do first  

![](https://i.ytimg.com/vi/UYyqQD3w59c/maxres1.jpg)



#### [0:00:30](https://www.youtube.com/watch?v=UYyqQD3w59c&t=30) |  is we import this class from the

"pathlib" module using the combination of from and import commands. This command allows you to import just a part of a module. So now that we've imported the Path class we can move forward and create a Path object. And in this case, we create a Path object which points towards a directory called "data". Now that we have the Path object stored under a variable,  

#### [0:01:00](https://www.youtube.com/watch?v=UYyqQD3w59c&t=60) |  we can explore some of the useful

methods and attributes that are available for the Path object. We could, for example, start by checking if the path is actually valid using the "exists" method, so we check if the directory exists. We can also check if the directory is actually a directory which is also true ,and then finally we should check that the directory isn't actually a file  

![](https://i.ytimg.com/vi/UYyqQD3w59c/maxres2.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=UYyqQD3w59c&t=90) |  which returns the value false. So now

that we know that the Path object points towards a directory we can use the "glob" method to collect all the text files in this directory. The "glob" method requires just one argument, pattern which takes a string as an input. This string can be used to define the types of files that you want to collect you can use the asterisk symbol as a wildcard  

![](https://i.ytimg.com/vi/UYyqQD3w59c/maxres3.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=UYyqQD3w59c&t=120) |  to refer to any sequence of characters

in order to match the file names. So in this case we're looking for text files which commonly have the suffix .txt. So we use the glob method to look for text files and then we cast the result into a Python list, and finally we call the result to check which files are contained in the directory. So if we call the variable we see that it's a list  

#### [0:02:30](https://www.youtube.com/watch?v=UYyqQD3w59c&t=150) |  containing paths to three text files in

the directory. Now that we have a list of files we can loop over each file, open it for reading, read the contents, manipulate them and then finally we can use the "close" method to close the file after doing whatever we need to do. I hope you found this video useful and if you have any questions, just leave a comment below. See you soon!  