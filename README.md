# SpamFiltering-NaiveBayesAlgo
### Problem:
To predict whether a new mail based on its content, can be categorized into spam or not-spam.

1. Loading the data 
2. Basic Checks
3. Text Preprocessing:

Step-I: 
Is to remove punctuation from the text/message/record:
We just created a simple function to remove punctuation from a text:
a. we'd created an empty list
b. char for char in text means whatever msg or text we pass 'char' starts traversing and 
c. if not in string .punctuation means check for the characters which are not present in punctuation signs , basically it          compares the characters with punctuation signs.
d. Then, cleaned data'll join with that empty list and return the cleaned text.

Step-II:
Add cleaned text column in the dataset.

Step-III:
Tokenization: Process of converting the normal string data into a list of tokens (also known as lemmas). OR
It consists of splitting an entire text into small units (tokens).
CountVectorizer :
It'll help us convert a collection of text documents to a vector of token counts.
That counts the number of times a word was mentioned in doucuments.
"Stopwords are the words in any language which does not add much meaning to a sentence. They are the words which are very common in text documents such as a, an, the, 
you, your, etc. The Stop Words highly appear in text documents. However, they are not being helpful for text analysis in many of the cases, So it is better to remove 
from the text. We can focus on the important words if stop words have removed.

4. Model Building
5. Created a simple application in which we pass any mail as a sample and check whether it is spam or not.

6. After that we used Tf-Idf vectorizer and then built a model using that:
Firstly lets understand what is Tf-Idf

Tfidf :
In BOW approach we saw so far, all the words in the text are treated equally important. There is no notion of some words in the document being more important 
than others. 
TF-IDF addresses this issue. It aims to quantify the importance of a given word relative to other words in the document and in the
Term Frequency (tf) TF: Term Frequency, which measures how frequently a term occurs in a document. Since every document is different in length,
it is possible that a term would appear much more times in long documents than shorter ones. Thus, the term frequency is often divided by the document length 
(aka. the total number of terms in the document) as a way of normalization:

TF(t) = (Number of times term 't' appears in a document) / (Total number of terms in the document).

Inverse Document Frequency (idf) It measures how important a term is. While computing TF, all terms are considered equally important.
However it is known that certain terms, such as "is", "of", and "that", may appear a lot of times but have little importance. 
Thus we need to weigh down the frequent terms while scale up the rare ones, by computing the following:

IDF(t) = log_e(Total number of documents / Number of documents with term t in it).corpus. It was commonly used representation scheme for information retrieval systems, 
for extracting relevant documents from a corpus for given text query.

Let's see an example:

Consider a document containing 100 words wherein the word cat appears 3 times.

The term frequency (i.e., tf) for cat is then (3 / 100) = 0.03.

Now, assume we have 10 million documents and the word cat appears in one thousand of these.

Then, the inverse document frequency (i.e., idf) is calculated as log(10,000,000 / 1,000) = 4.

Thus, the Tf-idf weight is the product of these quantities: 0.03 * 4 = 0.12

7. Lastly, we defined the pros and cons. of this algorithm.

