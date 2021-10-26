[![#5 Text formats and encoding](https://i.ytimg.com/vi/P-om89HKx80/maxresdefault.jpg)](https://www.youtube.com/watch?v=P-om89HKx80)

## #5 Text formats and encoding

In this video, we will talk about rich, plain and structured text, how text is encoded and what this means to manipulating text using Python.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/01_basic_text_processing.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=P-om89HKx80&t=0) |  Hi! In this video I'm going to

tell you about how computers store and represent text and what this means for processing texts using Python. As you can see, I already have a notebook open and you can find a link to this notebook in the description below. First of all let's get started with computers and text. So computers can store and represent text in different formats which are 1. rich text, 2. plain text and 3. structured text. So if you've ever used a  

#### [0:00:30](https://www.youtube.com/watch?v=P-om89HKx80&t=30) |  word processor like Microsoft Word then you

will probably have worked in rich text. Rich text is essentially text whose appearance has been formatted or styled in a specific way, so rich text essentially allows you to define different visual styles for document elements. So maybe you could have a document header in one slightly larger font than let's say the body text  

#### [0:01:00](https://www.youtube.com/watch?v=P-om89HKx80&t=60) |  and so on and so forth. Rich

text is challenging for programming languages to process because these features the different visual styles are encoded into the document itself. So in short rich text is the default format for modern word processors. The next type of text is the so-called plain text which does not contain any information about the visual appearance of text, but it simply consists  

![](https://i.ytimg.com/vi/P-om89HKx80/maxres1.jpg)



#### [0:01:30](https://www.youtube.com/watch?v=P-om89HKx80&t=90) |  of characters only. What is meant by

characters in this context is letters numbers punctuation marks spaces and line breaks, for example. Generally plain text refers to text that lacks any kind of formatting or style information. The third alternative, structured text, is a special case of plain text which also includes some character sequences which are used to format the  

#### [0:02:00](https://www.youtube.com/watch?v=P-om89HKx80&t=120) |  text when it's rendered for display. Examples

of structured text include markup languages like XML markdown or HTML because we can take a look at this example right here which contains an example sentence "this is an example sentence" which has been wrapped into tags consisting of the opening tag  and the closing tag  and the computer will know based on these tags that this particular  

#### [0:02:30](https://www.youtube.com/watch?v=P-om89HKx80&t=150) |  sentence is to be rendered as a

paragraph when rendered for display. So why does this matter? If you want to use Python to manipulate text then you'll need plain text if your data is stored in rich text. Let's say if you would be working with some transcripts of spoken dialogue in which the format or visual appearance of text contains some information about the language use or the speakers  

![](https://i.ytimg.com/vi/P-om89HKx80/maxres2.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=P-om89HKx80&t=180) |  themselves then what you want to do

is ensure that this information gets carried over to the plain text as well. Or if you work with digital documents that you've collected from websites or discussion forums then you need to be extra careful not to carry any of that structured text into your plain text corpus. So in other words you need to pay attention to the process  

#### [0:03:30](https://www.youtube.com/watch?v=P-om89HKx80&t=210) |  of converting rich unstructured text into plain text

for processing using Python. Once you have plain text you need to pay attention to text encoding. To enable computers to read text, the text has to be encoded into a numerical representation and this is commonly done using character encoding which is simply a process that maps each character  

#### [0:04:00](https://www.youtube.com/watch?v=P-om89HKx80&t=240) |  such as a letter or a number

or a punctuation mark to a specific numerical representation for the computer. In an ideal world we would never ever have to deal with low-level stuff like character encodings but unfortunately there are multiple systems for character encodings which are not compatible with each other. There are two main types of character encoding systems  

![](https://i.ytimg.com/vi/P-om89HKx80/maxres3.jpg)



#### [0:04:30](https://www.youtube.com/watch?v=P-om89HKx80&t=270) |  that you're likely to encounter the first

one is ASCII and the second one is Unicode. ASCII stands for American Standard Code for Information Interchange and it is a slightly older but pioneering character encoding system. One feature of ACII is that it's very limited in terms of its character range so for example if your language happens to be Finnish and includes characters like a or o with dots then you cannot encode these characters using ASCII.  

#### [0:05:00](https://www.youtube.com/watch?v=P-om89HKx80&t=300) |  The modern alternative is called Unicode which is

a standard for encoding text in most writing systems used in the world. For example the pizza slice emoji has the unicode code U+1F355 which is unique for the pizza slice and each one of the 140 000 characters has its own unique code like this. Unicode is a standard that can be implemented in different  

#### [0:05:30](https://www.youtube.com/watch?v=P-om89HKx80&t=330) |  character encodings such as UTF-8 which is

defined in the Unicode standard UTF-8 also happens to be the standard character encoding system for Python 3. UTF-8 is also backwards compatible with ASCII which means that you can decode files that have been encoded using ASCII into UTF-8. To sum it up,  

#### [0:06:00](https://www.youtube.com/watch?v=P-om89HKx80&t=360) |  when working with text in Python you

want to use UTF-8 encoding. I hope you found this video useful and if you have any questions just leave a comment below and hope to see you soon!  