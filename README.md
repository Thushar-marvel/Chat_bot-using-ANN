# Chat_bot creation using ANN

A chatbot is an artificial intelligence (AI) software that can simulate a conversation (or a chat) with a user in natural language through messaging applications, websites, mobile apps or through the telephone.
A chatbot is often described as one of the most advanced and promising expressions of interaction between humans and machines. However, from a technological point of view, a chatbot only represents the natural evolution of a Question Answering system leveraging Natural Language Processing (NLP). Formulating responses to questions in natural language is one of the most typical Examples of Natural Language Processing applied in various enterprises’ end-use applications.


![image](https://user-images.githubusercontent.com/69953585/110901008-a6c8b000-8329-11eb-8458-c17a3c4e6a37.png)


# Procedure
# Load libraries
NLTK -The Natural Language Toolkit (NLTK) is a platform used for building Python programs that work with human language data for applying in statistical natural language processing (NLP). It contains text processing libraries for tokenization, parsing, classification, stemming, tagging and semantic reasoning.
Numpy - To work with array
Tensorflow - To create model
json - To work with json file
pickle - To save pre processed word vector in pickle format

# Data
Intend file is created which is in json format. This file consists of set of tags and for each tag set of predefined questions along with answers.

# Data loading and pre processing
Intend file is loaded and converted it as list of words.Tokenization is done using nltk library (converting sentence to seperate words).
![image](https://user-images.githubusercontent.com/69953585/110900881-784ad500-8329-11eb-96c3-15393c872317.png)

Each word in the query/ question is normalized using stemming method(convert word to its base form)
The intend file has 20 tags and total number of queries are 83
Training file is created which is  Word matrix with row=Number of queries and column=Number of words
output label is created similar to above with row=Number of queries and column=Number of tags
if word present in the query then matrix element value will be 1 else 0 and so on.

# ANN model
With the help of tensorflow as backened ANN model is built with 2 hidden FC layers and final output softmax layer.Used Adam optimizer.Trained the model for 1000 epochs and saved it as tflearn model for future use.Achieved best accuracy of 97.3%

![image](https://user-images.githubusercontent.com/69953585/110901721-c14f5900-832a-11eb-81c7-62ab2b9809fb.png)





   
   
Further improvement can be done by training it with more set of questions and answers and built GUI to run this program.   
