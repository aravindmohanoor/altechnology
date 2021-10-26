[![#4 Getting started with Python: variables and objects](https://i.ytimg.com/vi/65u7GK9c78o/maxresdefault.jpg)](https://www.youtube.com/watch?v=65u7GK9c78o)

## #4 Getting started with Python: variables and objects

In this video, we will learn about two fundamental concepts in Python: variables and objects.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_i/02_getting_started_with_python.html 



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Getting Started playlist: https://www.youtube.com/playlist?list=PL6cQi6qFlek2G1okRUjmFtiP_0e6MHJFN



#### [0:00:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=0) |  Hi! In this video I'm going to

introduce you to two fundamental concepts in Python: variables and objects. As you can see, I already have a notebook open. You can find a link to this notebook in the description below. So let's get started with the notion of a variable. To put it very simply, variables are just unique names for various kinds of objects defined in a program. If you think about it, every object needs to have a name so it can be referred to  

#### [0:00:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=30) |  elsewhere in the program. In Python variables are

assigned using a single equal sign. The name of the variable is positioned on the left hand side of the equal sign, whereas the object that the variable refers to is on the right hand side of the equal sign. So let's go ahead and define our first variable in this notebook. If you take a look at this code cell, what we do here is we use  

#### [0:01:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=60) |  the equal sign to define a variable

named "var" which has a string object as its value. The string object is a particular type of object, which consists of sequences of characters and they are always marked using single or double quotation marks. So in this case we assign a string with the text "this is a variable" to the variable in question. So let's go ahead and execute this cell.  

#### [0:01:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=90) |  As you can see the number in

the brackets was updated, so this cell was executed and no error was raised so everything seems to be fine and now we can move forward and call the variable. This returns the object that the variable refers to, and as the notion of a variable suggests the value of a variable can also change. So what we're going to do here is we're going to simply  

#### [0:02:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=120) |  update the value of the variable; so

we're going to assign another string object to the same variable so this is what happened. And now if I execute this cell again, I call the variable then we will have the updated value for the variable. So as you can see, the string was updated. Sometimes you also need to have variables ready before they're even defined, and in this case it's  

![](https://i.ytimg.com/vi/65u7GK9c78o/maxres1.jpg)



#### [0:02:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=150) |  quite useful for to define some placeholders

for some objects. You might have noticed that there are no quotation marks around the text "None" and this is because None is not a string object, it's a specific type of object called a NoneType object. Although variable names can be chosen pretty much freely, they should be informative and you should also keep in mind that the variable names are case sensitive. So let's give this a try and call the variable by capitalizing  

#### [0:03:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=180) |  the variable name and if we execute

the cell right now we will get an error. This error message tells us that there is a NameError, and more specifically the name var with a capital V is not defined. There are also some limitations to naming variables in Python, so some words are  

#### [0:03:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=210) |  reserved for Python itself. We can easily

check these words by importing a module using the import command which we are going to use quite frequently in this course. So if we execute the cell then we will import a module named keyword and then we will assign a part of the module to a variable named keywords, and finally we will print out what is stored under the variable keywords.  

#### [0:04:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=240) |  In this case we get a list

of keywords that have been reserved for the Python programming language. So what we did here is that we imported a module which has an attribute called kwlist which contain this list of keywords. So these are practically the words that cannot be used as variable names and if you try to do so then typically the environment in which you use Python will probably  

#### [0:04:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=270) |  warn you about this. So I already

referred to the object now stored under the variable keywords as a list, which is just one type of object defined in Python. It's often useful to know what kinds of objects you're dealing with, because the type of the object determines its behavior in Python. So if we want to check out the type of a object we can use a type function from Python and just place  

![](https://i.ytimg.com/vi/65u7GK9c78o/maxres2.jpg)



#### [0:05:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=300) |  the name of the object or the

name of the variable within the parenthesis of the function as we do in this cell, and as you can see this returns the type of the object. So in this case we're dealing indeed with a list. We can also check the type of the previous variable that we gave the name var and if we execute this cell then we'll get the output which is a NoneType. As I already said,  

#### [0:05:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=330) |  the type of a Python object determines

its behavior. For example, we can use brackets to access items in a list, so if we execute this cell right here and access the fourth item in the list under the variable keywords. If you're wondering why the number three is here and stands for the fourth item that's because lists are zero-indexed so counting begins from zero in Python. And if we  

#### [0:06:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=360) |  execute the cell then we'll get the

string object and as the output. So this is the fourth item in the keywords list. What if we try to do the same to the variable var which stores a NoneType? So if we execute the cell then we'll get a TypeError message saying that the Nonetype object is not subscriptable. So let's go back to the list of keywords if we want to check the type  

#### [0:06:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=390) |  of the fourth item in the list

of keywords we can use the type function and by executing this cell right here we'll see that the list contains string objects and this is entirely common so Python objects may be nested within other objects. So what I want to do next is to define another example which consists of a string object that contains some text and there's also some HTML tags  

#### [0:07:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=420) |  within the text. So if we execute

the cell and then print out the string object, we get the text and now what we can do next is we can use some of the methods that are provided for string objects. One of these methods is the split method, which can be used to split a string into a list. To split the object into a list we want to do a couple of steps. So first of all  

#### [0:07:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=450) |  we're going to assign the output into

a new variable and in this case we're going to give the variable the name tokens and what we then on the right-hand side of the equal sign; what we're going to do is we take the text variable which contains the string object and then we call the split method and we can see the method here it's separated from the  

![](https://i.ytimg.com/vi/65u7GK9c78o/maxres3.jpg)



#### [0:08:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=480) |  variable with a full stop and then

in the parentheses following the split method here we have a argument named sep which stands for the separator. So the character that will separate the items in the string, and in this case we have an empty space right here, so we separate or we split the string at whitespace. If we call the variable then we will get a list of string  

#### [0:08:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=510) |  objects. It's important to keep in mind

that the split method is destructive, so something that is used for splitting the string is always removed from each string in the resulting list. So you can see for example that in this output the less than characters have disappeared from the string items in the list. Now finally I want to go back to the original example that we had  

#### [0:09:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=540) |  stored under the variable text, which contains the

example string with some HTML tags thrown in. We can now try out another method named replace that we could use for example if we would like to replace the HTML tags or remove them from our example string, and for this purpose we can use the replace method that allows replacing  

#### [0:09:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=570) |  specific characters or sequences in a string and

let's just begin by removing the initial tag  from the text. So what we do here is we provide two strings as input to the replace method and as you can see the two strings are separated by a comma so the first part stands for the  

#### [0:10:00](https://www.youtube.com/watch?v=65u7GK9c78o&t=600) |  pattern or the sequence of characters that we're

looking for and the second one defines the replacement. So in this case we're looking for the opening tag and then we're replacing it with an empty string. Now if we execute this cell and then look at the output we'll see that the opening tags have disappeared so in this case the tag at the very beginning of the string is gone. So this concludes the first notebook which provided a very brief introduction  

#### [0:10:30](https://www.youtube.com/watch?v=65u7GK9c78o&t=630) |  to two fundamental concepts in Python, variables and

objects, which we will then expand on in later notebooks while also learning more about processing text using Python. I hope you found this video useful; if you have any questions leave a comment below and see you next time!  