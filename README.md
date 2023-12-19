# How to achieve glory and success as a filmmaker

## Datastory

A movie producer comes to see us and says he wants to make a successful movie in a given genre and for a given geographical area, between USA, America, Africa, Europe, Asia or Oceania. He wants to find the best drivers that will make his movie a success, both financially by making substantial box office profits, and critically by getting good ratings and reviews. We decided to create an easy-to-use interface where the producer can select his genre and target market parameters and get feedback on the optimization of multiple parameters such as runtime, director profile, actor profiles, main language, and potentially plot and character persona elements in order to achieve his goal. 

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

## Additional datasets

As we are computing a success rating for each movie, we need to take into account the reviews, the inflation adjusted profits to be able to compare the profitability of each movie and the Oscars nominations and awards. This data is not available in the provided datasets. We use these additional datasets in order to get them:

- Database online: [IMDb free database](https://developer.imdb.com/non-commercial-datasets/) 
- Data scrapping of IMDb reviews (if we have time): [IMDb scores](exploration/IMDb_scrapping_v1.ipynb)
- Data for movie budgets : [TMDB dataset](https://www.kaggle.com/datasets/kakarlaramcharan/tmdb-data-0920)
- Oscars nominations and wins dataset : [Oscars](https://www.kaggle.com/datasets/pushpakhinglaspure/oscar-dataset)
- Dataset used to compute inflation adjusted profits : [US inflation data](https://www.kaggle.com/datasets/varpit94/us-inflation-data-updated-till-may-2021)

## Method

### Part 1: Define the metrics

**Step 1:** We need to define how we can measure the success score and what success means. Based on the enriched datasets, several indicators could work: number of awards (Oscar, César, etc.), box office, reviews, IMDb scores, etc (cf. jupyter notebok).

**Step 2:** As we want to compare films based on the different types of genre, we need to analyze the distribution of genres across the database. We also need to select which genres to focus on (accroding to the availability of the data).

**Step 3:** We should do the same as the step 2 but for the location. If we only keep the countries, we will have too few data per country, so we need to define bigger location such as mainland. 

**Step 4:** We have to select the other parameters that could also be relevant like: 
- Latent personas (from Learning Latent Personas of Film Characters, David Bamman Brendan O’Connor Noah A. Smith): personnas in a successful action movies will differ from those in a successful romantic comedy. 
- Language
- Movie runtime
- Famous actors
- Age/gender of actors
- Plot of movies : analyzing popular themes (use of NLP to extract a theme for each movie)

### Part 2: Merge & Clean the data

**Step 5:** Load the initial datasets and clean the  data. For example we need to have all the date in the same format, we delete the NaN, we clean the textual data. We removed some unnecessary columns (movie ID, freebase ID). 

**Step 6:** Classify the genres and the mainland as defined in step 2 and 3. 
- For the list, we keep the top 10 genres in the dataset.
- For the locations we map the country to its mainland (Europe, Asia, Africa, America, Oceania, USA) and we make an exception for the USA because it already represents a huge proportion of the dataset.

**Step 7:** Merge the additional datasets. We merge based on release date, title, year and finally on IMDB ID in order to add the author of the film. As a final step, to add the inflation rate, we left merge on the year so that we can compare box office revenue.

**Step 8:** Check the feasibility of the scientific questions by checking the data availability. For each question, have we got enough data to answer it? Plot some graphs that can explain/show the feasability.

### Part 3: Analysis & Datastory

**Step 9:** Answers to scientific questions in response to our problem. This step is key for the analysis because it will highlight the parameters for the best movie according to a specific genre and location.

**Step 10:** Implement ML Algorithm such as RandomForest and CatBoost models to analyze movie success based on Main Language, Main Country, and Runtime, focusing on top genres. Our approach includes preprocessing steps like categorical encoding and feature scaling. Future expansions will integrate more features, such as genre and budget, enhancing our model to offer deeper insights into what drives movie success.

**Step 11:** Design an easy-to-use interface for the client. The user must be able to select the movie genre and the country where he wants to produce the movie, and then we show him the important criteria for a successful film.

## Executed timeline

03.11.2023 : Part 1

**Milestone 2** - 17/11/2023 : Part 2 

10.12.2023 : Step 8 & 9

20.12.2023 : Step 10 & 11

**Milestone 3** - 22/12/2023 


## Organization within team
| Teammate | Role|
| --- | --- | 
|**Aline** |***|
|**Mathieu**|***| 
|**Benoit**|Causal analysis + interface content & design + ReadMe| 
|**Antoine**|***|
|**Valentin**|***|


## BAVMA Research Team

This projects takes place in the context of the ADA 2023 course at EPFL Lausanne.

The team members are : 

- Aline Janvier
- Benoît Gallois
- Valentin Parisot
- Mathieu Faure
- Antoine Goupil de Bouillé

