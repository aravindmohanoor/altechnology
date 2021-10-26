[![#8 Regular expressions](https://i.ytimg.com/vi/seCpHdTA-vs/maxresdefault.jpg)](https://www.youtube.com/watch?v=seCpHdTA-vs)

## #8 Regular expressions

In this video, we will learn about regular expressions and how to use them in Python. 



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/02_basic_text_processing_continued.html#Regular-expressions



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=seCpHdTA-vs&t=0) |  Hi! In this video I'm going to

introduce you to regular expressions and how they can be used to find and replace patterns in Python string objects. As usual, I already have a notebook open and you can always find a link to this notebook in the description below. Regular expressions is a language that allows you to define patterns that can be then matched against some text or sequence of characters. Python allows you to use regular expressions using a separate module called "re",  

#### [0:00:30](https://www.youtube.com/watch?v=seCpHdTA-vs&t=30) |  which stands for regular expressions. We can easily

activate this module by importing the module using the import command, and if we execute this cell now we have the re module available for this notebook. What we're going to do next is we open and read the contents of a text file and print out some of the result, and as you can see this text which has been digitized using  

![](https://i.ytimg.com/vi/seCpHdTA-vs/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=seCpHdTA-vs&t=60) |  optical character recognition shows quite a lot of

errors so you have sequences of various punctuation marks and other non-alphanumeric characters that are pretty much just errors. So what we're going to do next is we compile a regular expression that searches for sequences of two or more full stops and we're going to do this using the compile  

#### [0:01:30](https://www.youtube.com/watch?v=seCpHdTA-vs&t=90) |  function from the re or regular expressions

module in Python. The compile function takes a string as input and what we're going to do here is we define a new variable named "stops" after our pattern and then we call the compile method from the re module, and feed a string to this function. This string object is preceded by the letter r which tells Python to store the string  

#### [0:02:00](https://www.youtube.com/watch?v=seCpHdTA-vs&t=120) |  in raw format which means that the

string is stored exactly the way it appears here. This is just to ensure that the regular expression is stored exactly in the way that we want it to be stored. To compile the regular expression we simply run this cell which then returns us  

![](https://i.ytimg.com/vi/seCpHdTA-vs/maxres2.jpg)



#### [0:02:30](https://www.youtube.com/watch?v=seCpHdTA-vs&t=150) |  the type of the "stops" variable which

is a pattern object. So what I want to do next is to unpack this expression just a little bit. So we started off by defining a Python string which you can recognize by looking at the surrounding quotation marks. Within these quotation marks, the first two characters are the backslash and the full stop and we need this backslash here  

#### [0:03:00](https://www.youtube.com/watch?v=seCpHdTA-vs&t=180) |  to tell Python that we're actually referring to

a full stop, because regular expressions use the full stop as a wildcard, which means a character that can stand in for any character. So this full stop in a regular expression could stand in for a question mark or the letter a or whatever, but we need to define that this is a actual full stop and that's why we need  

#### [0:03:30](https://www.youtube.com/watch?v=seCpHdTA-vs&t=210) |  the backslash character here. What comes next within

the curly brackets is a quantifier that instructs the regular expression to look for the preceding pattern, that is, the actual character full stop that occurs two or more times in a row. So now we have a regular expression that has been compiled into a pattern object and in order to make some use of this object  

![](https://i.ytimg.com/vi/seCpHdTA-vs/maxres3.jpg)



#### [0:04:00](https://www.youtube.com/watch?v=seCpHdTA-vs&t=240) |  and apply to some text we can

call the "sub" method which is available for the pattern object which we stored under the variable "stops", and the "sub" method takes two arguments. The first one is called "repl", which is a string object that contains the string that is used to replace possible matches, so you can think of this as the replacement. The second one called "string"  

#### [0:04:30](https://www.youtube.com/watch?v=seCpHdTA-vs&t=270) |  is an argument that defines the string

object to be searched for matches. And what we get back from the sub method is a modified string object that contains the string object that we provided to the string argument. So what we do in this cell we call the "sub" method from our Pattern "stops" and we look for matches in the string object named "extract" and then store the returned  

#### [0:05:00](https://www.youtube.com/watch?v=seCpHdTA-vs&t=300) |  string object under the variable of the

same name. Now if I run this cell you'll see that the sequences of full stops are gone from the text, but otherwise it remains completely the same. I hope you found this video useful and if you have any questions, feel free to leave a comment below.  