# Reddit Topic Modeling

## Description
This project performs topic modeling on Reddit comments using Python. It utilizes `praw` for Reddit API access, `nltk` for text preprocessing, and `sklearn` for topic modeling with LDA.

## Usage
- Download the python script I have uploaded
- Create Reddit account and set up application to get `CLIENT_ID`, `CLIENT_SECRET` and `USER_AGENT`.
- Replace them in the script
- Get the url of the reddit page
- Run the script

## My Take on the Project

This is a project that I did by myself for the first time in NLTK.
- PRAW (Python Reddit API Wrapper): Used to interact with Reddit’s API to fetch comments from a specific Reddit thread.
- NLTK (Natural Language Toolkit): Utilized for text preprocessing, including tokenization, stopword removal, and lemmatization.
- Scikit-learn: Employed for feature extraction using CountVectorizer and topic modeling using Latent Dirichlet Allocation (LDA).
  
These tools are used to preprocess Reddit comments, convert them into a format suitable for machine learning, and perform topic modeling to identify key themes in the comments.

I have used LDA as the NLTK model.

- Purpose: LDA helps in identifying the underlying topics that are present in a set of text data, such as Reddit comments.
- Mechanism: It assumes that each document is a mixture of a small number of topics and that each word in the document is attributable to one of the document’s topics.
- Process: The model iteratively assigns words to topics based on their co-occurrence patterns, refining the topic distribution for each document and the word distribution for each topic.
- Output: The result is a set of topics, each represented by a distribution of words, and each document represented by a distribution of topics.

## Results

I ran a thread about Elon Musk: https://www.reddit.com/r/IAmA/comments/2rgsan/i_am_elon_musk_ceocto_of_a_rocket_company_ama/

```output
PS C:\Users\Phantom\Documents\DS\Projects> python reddit.py
Enter the Reddit thread URL: https://www.reddit.com/r/IAmA/comments/2rgsan/i_am_elon_musk_ceocto_of_a_rocket_company_ama/

Topics in the Reddit thread:
Topic 1: spacex like launch space tesla time
Topic 2: space kerbal rocket program space program kerbal space
Topic 3: like work think good thing elon
Topic 4: elon musk elon musk question work sleep
Topic 5: got mars year von going von Braun

```
