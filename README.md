# How to achieve glory and success as a filmmaker

## Datastory

A movie producer comes to see us and says he wants to make a successful movie in a given genre: Drama, Comedy, Action and advendture, science-fiction and Horror. He wants to find the best drivers that will make his movie a success, both financially by making substantial box office profits, and critically by getting good ratings and reviews. We decided to create an easy-to-use interface where the producer can select his genre and target market parameters and get feedback on the optimization of multiple parameters such as runtime, director profile, actor profiles, main language, and potentially plot and character persona elements in order to achieve his goal. 

You can access our datastory by clicking [here](https://antoine2bouille.github.io/).

## Abstract

In this study, we seek to uncover the ingredients that will make the perfect film, so as to achieve success and glory at the Oscars ceremony. To do this, we begin by examining the relationship between ImbD scores and the 5 main film genres (Drama, Family, Action/adventure, Science-Fiction & Horror). We then separate the analysis feature by feature, starting with the study of the best screen time, then check the link between winning an award and subsequent revenues and ratings. Finally, we compare different aspects depending on the continent on which the film is released.

This first study enables us to set the framework for our study, so that we can go into more detail in the analysis when we look at a particular genre.

To finish our study and offer the reader a concrete solution, we go through each genre one by one to determine what the succesfull drivers are, such as the themes tackled, the 5 countries in which the film will be the most successful, the languages and finally the perfect casting and film director.


## Research questions
These are some of the research questions we're going to try to answer. They will provide a common thread for our analysis and lead us to the elements for a masterpiece.

- Which genre is more represented according to a location? Which genre performs better according to a location?
- Which relation between the screen time and the opportunity to win an award ?
- What is the relation between revenues and being awarded?
- What is the relationship between ratings and revenues?
- How do rating and revenue vary as a function of the genre?
- What is the optimal runtime for each genre?
- Does the cast influence the gender, the revenue amount and the rating?
- What are the key main themes explored in a given genre? 

## Additional datasets

As we are computing a success rating for each movie, we need to take into account the reviews, the inflation adjusted profits to be able to compare the profitability of each movie and the Oscars nominations and awards. This data is not available in the provided datasets. We use these additional datasets in order to get them:

- Database online: [IMDb free database](https://developer.imdb.com/non-commercial-datasets/) 
- Data scrapping of IMDb reviews (if we have time): [IMDb scores](exploration/IMDb_scrapping_v1.ipynb)
- Data for movie budgets : [TMDB dataset](https://www.kaggle.com/datasets/kakarlaramcharan/tmdb-data-0920)
- Oscars nominations and wins dataset : [Oscars](https://www.kaggle.com/datasets/pushpakhinglaspure/oscar-dataset)
- Dataset used to compute inflation adjusted profits : [US inflation data](https://www.kaggle.com/datasets/varpit94/us-inflation-data-updated-till-may-2021)

## Methodology

Our final analysis focuses on 4 main analysis for each genre 

**Part 1: vizualization of key drivers for each genre** 

- This part extends our analysis in Milestone 2
- We explore the key links between variables for each genre using diverse plotting methods

**Part 2: using natural language processing to extrat relevant information from the plots**

- We first preprocess the plots using NLP techniques : lemmatization, stemmming, bag of words
- We use feature extraction techniques to find the main themes: use of empath and SpaCy libraries
- We also tried to use sentiment analysis analysis to find the negativity and positivity of plots. The analysis does not give significant results.

**Part 3: causal analysis of observational data**
- We explore the causal relationship between the fact of being awarded an Oscar and IMBD scoring
- We explore the causal relationship between the fact of being awarded an Oscar and revenue of the movie

**Part 4: using a machine learning pipeline**
This pipeline aims to explore for each genre:
- The countries where the movie should be released
- The most important languages of diffusion
- The optimal cast for each genre

**Part 5: designing an interface for the data story and results vizualisation**

## Executed timeline

03.11.2023 : Exploring the dataset and finding new usefull data

**Milestone 2** - 17/11/2023 : Part 1 

10.12.2023 : Step 8 & 9

20.12.2023 : Step 10 & 11

**Milestone 3** - 22/12/2023 


## Organization within team
| Teammate | Role|
| --- | --- | 
|**Aline** |Analysis of key drivers by genre|
|**Mathieu**|Understanding the perfect cast for a genre| 
|**Benoit**|Causal analysis + interface content & design + ReadMe| 
|**Antoine**|NLP analysis of main themes and website designing|
|**Valentin**|ML pipeline|


## BAVMA Research Team

This projects takes place in the context of the ADA 2023 course at EPFL Lausanne.

The team members are : 

- Aline Janvier
- Benoît Gallois
- Valentin Parisot
- Mathieu Faure
- Antoine Goupil de Bouillé

