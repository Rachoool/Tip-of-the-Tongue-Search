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


## Meeting notes for January 24, 2024
Time: 13:00PM - 13:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- Use context learing with university's api to give examples in the prompt to get the reasonable response
### Discussions at the meeting:
- Discuss the tasks for the next week
### Objectives for this week:
- Remove some of the features from the query that extracted before, and calculate the MAP score
- Check whether the original content of the movie contains the extracted content


## Meeting notes for January 31, 2024
Time: 13:00PM - 13:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- Remove some of the features from the query that extracted before, and calculate the MAP score
### Discussions at the meeting:
- Discuss th results already achieved
- Discuss the tasks for the next week
### Objectives for this week:
- Check whether the original content of the movie contains the extracted content and calculate the accuracy
- Extract the correct features from the corpus and re-add them to the query, and calculate the MAP at this point to see if there can be some improvement
- Consider about five research questions (two about age and three about extraction)


## Meeting notes for February 7, 2024
Time: 13:00PM - 13:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- Calculate the accuracy for these 5 features, but there is no genre in the wikidata
- Extract the correct features from the corpus and re-add them to the query, and calculate the MAP and nDCG 
- Five research questions:
  - Is it possible to identify the age of the person asking the TOT question
  - How to get the ages of these people
  - What are the main factors affecting the effectiveness of TOT
  - What factors do users mention when asking TOT questions
  - What is the impact of these factors on TOT as mentioned by the users
### Discussions at the meeting:
- How should research questions be asked
- What should the hierarchy of these questions be
- How to answer these questions
- add these factor for many times to see the importance of them
### Objectives for this week:
- Add factors for 5, 10 times and calculte MAP score
- Write the outline of dissertation


## Meeting notes for February 14, 2024
Time: 13:00PM - 13:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- Add factors for 5, 10 times and calculte MAP score
- Write the outline of dissertation
### Discussions at the meeting:
- Revising the details of dissertation outline
### Objectives for this week:
- Finish at least the Introduction and Background


## Meeting notes for February 28, 2024
Time: 13:00PM - 13:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- Finish the Introduction and Background
- Finish the Age Prediction and Key Factors in Methodology
### Discussions at the meeting:
- Discuss the method name of Feature deletion and Multi-Add Feature
- Add a diagram to Introduction
- Be aware of citation
- Add a brief introduction to each chapter
- Relate the related work to my research
- Some details of the use of words and sentences how to change some academic
- Add research question to Aim
- Adjust the order of paragraphs
### Objectives for this week:
- Finish Methodology
- Add some new section in Related Works
- Change the previous sections based on the issues discussed in the meeting
- Start to do the Experimental Setup


## Meeting notes for March 6, 2024
Time: 13:00PM - 13:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- Finish Methodology
- Add some new section in Related Works
- Change the previous sections based on the issues discussed in the meeting
- Start to do the Experimental Setup
### Discussions at the meeting:
- Change the sentences and words to be more academic
- Change the cited literature and do not cite wiki
- Add some recall to the chapter
- Add some introduction for subchapters
- Notice the space in the parentheses before the abbreviation
- Feature deletion and multi add feature, are introduced in detail
- Merge Sections 3.1 and 3.2
- Explain why these evaluation metrics are used
### Objectives for this week:
- Change the previous sections based on the issues discussed in the meeting
- Finish the dissertation


## Meeting notes for March 13, 2024
Time: 13:00PM - 13:30PM

Present: [Jiarui Li, Sean MacAvaney]
### Achieved in the previous weeks:
- Finish all the dissertation
- Change the previous sections based on the issues discussed in the meeting
### Discussions at the meeting:
- Summarize the results for the tables in the evaluation section
- Make some changes to the dissertation based on the feedback
### Objectives for this week:
- Make some change to the dissertation based on the issues discussed in the meeting
- Finish the presentation