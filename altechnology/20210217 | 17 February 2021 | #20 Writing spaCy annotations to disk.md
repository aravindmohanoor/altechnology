[![#20 Writing spaCy annotations to disk](https://i.ytimg.com/vi/zKvW8o-1wmk/maxresdefault.jpg)](https://www.youtube.com/watch?v=zKvW8o-1wmk)

## #20 Writing spaCy annotations to disk

In this video, I show you how to write texts processed using spaCy to disk.



✨ Check out the materials associated with this video on Read the Docs: https://applied-language-technology.readthedocs.io/en/latest/notebooks/part_ii/04_basic_nlp_continued.html



✨ Clone the repository with Jupyter Notebooks for interactive computing from GitHub: https://github.com/Applied-Language-Technology/notebooks



✨ Check out other videos in the Working with Text in Python playlist: https://youtube.com/playlist?list=PL6cQi6qFlek0rF-aCox3YHOWNdTZSFakA



#### [0:00:00](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=0) |  Hi again! In this video I'm going

to show you how to store spaCy Doc objects to disk. Before doing extensive processing using spaCy, it's important to try out your pipeline using a subset of the data. When everything works as intended you can proceed to process all of the text and store the result to disk. What you want to do is to process the texts once, store the results and load the results for further processing when needed. spaCy provides a special object class for storing Coc  

#### [0:00:30](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=30) |  objects and writing them to disk. This

class is called a DocBin and you can import it from the tokens submodule in the spaCy library. So what I'm going to do here is I'm going to import the DocBin object so we can write some docs on disk. What we want to do next is we create a DocBin object for storing the docs that we created in the previous video. So we provide the list of docs to the  

![](https://i.ytimg.com/vi/zKvW8o-1wmk/maxres1.jpg)



#### [0:01:00](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=60) |  "docs" argument of the DocBin object and then

we store the resulting DocBin object under the variable "docbin". If you've added some custom attributes to Docs, Spans or Token objects, then you need to also provide the argument "store_user_data" and set its value to True in order to preserve the custom attributes. So when I run this cell the DocBin has been created  

#### [0:01:30](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=90) |  and we can easily verify that all

three Docs made it into the DocBin by using the len method, and as you can see all of the three docs that we created in the previous video are now stored in the DocBin object. Once you have added all of the data into the DocBin object, you can use the to_disk method to write the document object to disk and for this purpose you need to provide a  

![](https://i.ytimg.com/vi/zKvW8o-1wmk/maxres2.jpg)



#### [0:02:00](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=120) |  single argument named "path" which points towards the

file to which the DocBin will be written, and by running this cell we write the DocBin object to disk to the path data/ docbin.spacy. When you want to continue working with your data you need to load the DocBin object from disk and to do so you need to first initialize an empty DocBin object and then use the from_disk method to  

#### [0:02:30](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=150) |  load the stored data from disk. So

what we do in this cell is we create a new variable named docbin_loaded and then call a DocBin object and note the parentheses here and then we call the from_disk method and provide the path argument and then give the path to the file  

![](https://i.ytimg.com/vi/zKvW8o-1wmk/maxres3.jpg)



#### [0:03:00](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=180) |  that we just created and then we

can just simply call the variable to examine the output and this gives us the document object. And finally in order to retrieve the Doc objects from the DocBin you need to use the get_docs method so what we do here is we create a variable named docs_loaded and then we cast the result into a list and then we provide the name of the  

#### [0:03:30](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=210) |  variable that refers to the document that

we just loaded, and then we use the getdocs method. And the get_docs method takes a single input that is the vocab attribute of a language object. This has to be the vocabulary of the model that was used to create the document object so that spaCy knows how to map the Docs to particular linguistic annotations. Then we can simply call  

#### [0:04:00](https://www.youtube.com/watch?v=zKvW8o-1wmk&t=240) |  this variable to check the result and

indeed those are the example sentences that we defined in the previous video. So just to summarize, you should ideally process all of your texts at once, then store the results and load them again for further processing. Thanks for watching; I hope you found this video useful and if you have any questions feel free to leave a comment below.  