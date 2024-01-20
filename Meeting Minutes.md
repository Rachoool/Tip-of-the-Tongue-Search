# Meeting Minutes

## Meeting notes for September 18th, 2023

Time: 1:30PM - 2:00PM

Present: [Jiarui Li, Sean MacAvaney]

### Discussions at the meeting:
* Discuss the concept of tip-of-the-tongue search and the process of filtering out less favourable ideas while retaining the good ones during a meeting.
* Explored how to use Google Scholar for finding and reading relevant literature.
* Gained some insights into information retrieval.
### Objectives for this week:
* Investigate more about tip-of-the-tongue phenomena by reviewing relevant literature, focusing on what others have discussed, methodologies used, and available data, and identifying valuable ideas to adopt while avoiding less useful ones.

## Meeting notes for September 25th 2023

Time: 12:30PM - 1:00PM

Present: [Jiarui Li, Sean MacAvaney]

### Achieved in the previous week:
- Reviewed 3 papers 
### Discussions at the meeting：
* Discuss how to get the age of the poster.
  - Get ethics approval
  - Create a new dataset
  - Find a public Reddit that shows the age of user
  - Infer a user's age based on other information they post
  - Use existing classifiers to predict the age of users
* Discuss three papers I saw last week
### Objectives for this week:
* Read the literature related to tip-of-the-tongue search and memory loss with age.


## Meeting notes for October 1st, 2023

Time: 12:30PM - 1:00PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous week:
- Samarth Bhargav has no other literature on TOT Search.
- Review papers:
  - On the Tip-of-Tongue: What cause word finding failures in young and older adults?
  - Lexical knowledge and Lexical retrieval in aging
  - Tip-of-Tongue in aging: Influence of vocabulary, working memory and processing speed
- all these papers do not provide a new dataset, their data came from volunteers of different age groups.
### Discussions at the meeting:
- Disscuss three papers I saw last week
- Decide to start experiments
### Objectives for this week:
- Look at the word with the existing Tip-of-the-Tongue dataset and build an index for the dataset
- retrieval with some method (BM25)
- learn tutorial
- Thinking about how to use Reddit to infer a user's age


## Meeting notes for October 19, 2023
Time: 16:00PM - 16:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous two weeks:
- Learn IR tutorial
- Learn Pandas's syntax about DataFrame
- Try to build index for dataset trec_tot_dev
- Try to retrieval with method BM25
### Discussions at the meeting:
- Find a dataset about user's age and their comments
### Objectives for this week:
- Follow the guide on github to run the PAN16-Author-Profiling database through classifier and make sure getting similar results.


## Meeting notes for October 27, 2023
Time: 15:00PM - 15:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous two weeks:
- Run Pre-Requisites correctly
- Problems running QuickStart
### Discussions at the meeting:
- Fixes an issue where QuickStart does not run successfully because of a version issue
### Objectives for this week:
- Run the AgePredictor model on Tip-of-the-Tongue dataset


## Meeting notes for November 6, 2023
Time: 12:30PM - 13:00PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous two weeks:
- Successfully run the trec-tot dataset on AgePredictor
- View results predicted with AgePredictor
- The range of predicted ages was found to be between 30 and 37.（The reason might be the distribution of the original AgePredictor's training set is different with the data I need to infer on age.）
### Discussions at the meeting:
- The AgePredictor Predictor is not accurate and how to find users' age based on the reviews they've used
### Objectives for this week:
- Find more age-related descriptions on websites and Reddit and get an estimate of how many users there are
- Considering other research directions, what else can we do with this dataset that doesn't depend on the age of the user


## Meeting notes for November 20, 2023
Time: 12:30PM - 13:00PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous two weeks:
- Use different keyword to search users‘ posts on websites that can be used to estimate users’ age
- Two alternative directions were considered
- Use crawler(beautifulsoup) to catch posts from users of my Remeber this Movie site in two categories (solved and unsolved)
### Discussions at the meeting:
- how to implement the direction about the users' mis remember
- how to use pyterrier to indexing and retreval
### Objectives for this week:
- Follow the pyterrier indexing demo to indexing for the text in corpus
- Follow the Retrieval and Evaluation colab to retrieval the queriers


## Meeting notes for December 11, 2023
Time: 12:30PM - 13:00PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- finish indexing for the text in corpus
- finish the retrival and evaluation for the queriers
### Discussions at the meeting:
- Discuss the correctness of the results of indexing and retrieval
### Objectives for this week:
- Use the GPT model (llama) to extract from the text what genre, actor or time it might be talking about


## Meeting notes for January 17, 2024
Time: 13:00PM - 13:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- Unable to use the univerisity's Llama api due to Connection error, and found another Llama api that could be used to carry out the extraction task
- Use Llama initially to extract the language, genre, character's name, city and release year from the text
### Discussions at the meeting:
- How to use the university's api
- The response generated was not the result my question intended
- How to avoid encountering api max_length limits
### Objectives for this week:
- Use the context learning approach with university's api to give examples in the prompt to get the expected response