[![#6 Loading text into Python](https://i.ytimg.com/vi/HMsoCeCn5rA/maxresdefault.jpg)](https://www.youtube.com/watch?v=HMsoCeCn5rA)

## #6 Loading text into Python

In this video, we will load a text file into Python and manipulate its contents. We will also learn about lists, tuples and for-loops in Python.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/01_basic_text_processing.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=0) |  Hi! In this video I'm going to

show you how to load plain text files into Python and how to manipulate their contents. As usual, I already have a notebook open and you can find a link to this notebook in the description below. If you want to load a plain text file into Python you need to use the open function and as you can see, if you look at this cell right here, the open function takes several arguments. The first argument is "file" which simply defines a path  

#### [0:00:30](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=30) |  to the file that you want to

open, whereas the second one is called "mode" and the mode argument defines the mode of access to the file. In this case we simply read the file contents. Finally, we explicitly declare the kind of character encoding used by the file which in this case is UTF-8 that was introduced in the previous video. If I execute this cell, Python will open the file  

#### [0:01:00](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=60) |  and assign the result into the variable

file. Now that I've executed the cell nothing happens, but if we want to check the output we can scroll down here and call the variable to examine the object, and as you can see the variable holds an object called TextIOWrapper: IO stands for input output which also has several attributes that correspond to the arguments that we provided to the open function. This is only the first step so now we have opened the file but we haven't read  

![](https://i.ytimg.com/vi/HMsoCeCn5rA/maxres1.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=90) |  the contents yet, so in order to

read the contents we need to move down here and use the read method of the TextIOWrapper object to read the file contents. Now that I've executed this cell we can scroll further down and look at the first 500 characters of this object and as you can see, what we have now under the variable text is an ordinary Python string object.  

#### [0:02:00](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=120) |  Because the object under the variable text

is a string, we have access to all the methods available for manipulating strings in Python, and just to give you an example, we can use the replace method to replace all character sequences that correspond to line breaks, that is, a forward slash and n (\n) with empty strings and store the result under a different variable. So if you take  

#### [0:02:30](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=150) |  a look at this cell right here,

you'll see that we call the replace method for the variable text and then provide two string objects as input to the replace method. These strings define the pattern that we want to find and replace, so the first one corresponds to the sequence that we're looking for and the second one corresponds to the replacement. And as you can see when I execute the cell  

![](https://i.ytimg.com/vi/HMsoCeCn5rA/maxres2.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=180) |  the resulting text under the variable process

text no longer includes line breaks. The replace method is a powerful tool but it gets a bit tedious if you have more than one pattern to replace, so one would need to define the replace operations on separate lines for each of the patterns. So finally I want to show you how to make the replace operation a bit more efficient by leveraging two Python data structures: lists and tuples. So what we're going to do first is we're going to define a  

#### [0:03:30](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=210) |  list that we assign under the variable

"pipeline" and we can create a list simply by placing objects within brackets. And as you can see here, these objects in this case consist of tuples, and the tuple is another data structure which is marked by parenthesis, and in this case  

#### [0:04:00](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=240) |  the tuple consists of two items and

these two items correspond to string objects that define the pattern to be located and then to be replaced using the replace method. So what I'm going to do next is I'll run this cell to create the list named "pipeline" and then we are going to use a for loop to loop over each item in this list. And to do so let's take a look  

#### [0:04:30](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=270) |  at this cell right here. So what

we're going to do next is we're going to loop over the "pipeline" list and we know already that the list consists of tuples that in turn consists of two string objects and the for loop starts with the command "for" which is then followed by two variables that are assigned on the fly during the loop and then these variables are followed  

![](https://i.ytimg.com/vi/HMsoCeCn5rA/maxres3.jpg)



#### [0:05:00](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=300) |  by the "in" command, which refers to the

object that is being looped over. So in this case we loop over each item in the pipeline list, and as you can remember the items in the list consist of tuples with two values and thus we need two variables after the "for" command here, and if you're wondering why we declare some variables here in the loop  

#### [0:05:30](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=330) |  it's simply because we want to be

able to refer to the objects in the list during the loop. And if you take a look at the next line of code here then you'll see that it has been somewhat indented from the "for" command and this is very important for "for" loops in Python so you always need to indent the lines of code that follow the "for" loop or are within the "for" loop. So what  

#### [0:06:00](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=360) |  we do here is we call the

replace method on the variable updated text and simply take the pattern in each tuple in the list which we can refer to using the variables alt and new and then we need to save the result so we update the variable by assigning the result into the variable updated text. Now if I execute this cell we'll get the updated text, so we've looped over  

#### [0:06:30](https://www.youtube.com/watch?v=HMsoCeCn5rA&t=390) |  all of the patterns in the pipeline

list and these patterns have been then applied to the string under the variable "updated text". I hope you found this video useful and if you have any questions feel free to leave a comment below and see you soon!  