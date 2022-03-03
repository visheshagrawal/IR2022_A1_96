# IR2022_A1_96

### Team: [Aditi](https://github.com/Soni-Aditi/), [Vishesh](https://github.com/visheshagrawal/)

Information Retrieval Assignment 1 

Question 1
## Preprocessing Steps
- Text conversion to lowercase.
- Tokenization using nltk.
- Lemmatization using WordNet Lemmatizer
- Removal of stop words using nltk.
- Special characters excluding alphanumeric are removed.
- All singly occurring characters are removed.
- Finally a set of all the words is created.

## Assumptions
- We assume that the queries would be case insensitive (regardless of whether the word is in capitals or small we treat it as same as long as it is the same word)
- Although we have used Lemmatizer, there is a chance that not all tokenized words get lematized properly.

## Methodology
- First of all from all the docs present in the dataset we walked through it, and make a mapping.json file where we have a list of paths to all documents in a dataset.
- Then we iterate over all the file paths and read the file.
- Then we use our preprocessing function (all preprocessing steps are mentioned above), and tokenize the text.
- Now we store these values in a dictionary where each word is stored as a key, and a count is maintained for the doc as well as the number of occurences in it for that word.
- We have used OR, AND, NOT operands and number of comparisons have been computed using the merge algorithm for 2 key words' posting list
- Finally we report the number of docs matched as well as number of comparisons.

Question 2

## Preprocessing Steps
- Text conversion to lowercase.
- Tokenization using nltk.
- Removal of stop words using nltk.
- Special characters excluding alphanumeric are removed.
- All singly occurring characters are removed.
- Finally a set of all the words is created.

## Assumptions
- We assume that the queries would be case insensitive (regardless of whether the word is in capitals or small we treat it as same as long as it is the same word)

## Methodology
- First of all from all the docs present in the dataset we walked through it, and make a mapping.json file where we have a list of paths to all documents in a dataset.
- Then we iterate over all the file paths and read the file.
- Then we use our preprocessing function (all preprocessing steps are mentioned above), and tokenize the text.
- Now we store these values in a dictionary where each word is stored as a key, and a count is maintained for the doc as well as the number of occurences in it for that word.
- This positional encoding is then saved.
- Now for the query, we first take the input. Then we preprocess it using the same method.
- From the query we get the postings and the docs related to it.
- Then we find the intersection between lists and find docs which have all the words in the query.
- Finally we report the number of docs as well as which all docs.
