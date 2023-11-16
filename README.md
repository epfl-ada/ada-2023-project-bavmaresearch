# How to achieve glory and success as a film maker

## Datastory

A producer comes to see us and wants to make a successfull movie in a given genre and for a geographical-area. He wants to find the best drivers that will make his movie sucessfull. We decided to create an easy-to-use interface where the producer can select his parameters and find a way to make the film that will bring him fame and success. 

You can access the interface by clicking on the link: *Coming soon*


## Abstract

When you arrive at the interface, you can choose the genre of the film you want to make, as well as the geographical area in which it will be released. 
To determine the parameters that will bring fame to our client, we search for links among similar successful films. To find out whether a film is a success or not, we give it a score based on awards (Oscars, nominations...), ratings and budgets.
We then look at whether budget has a major influence on success, as well as screen time, choice of actors and other parameters.

## Research questions

- Which genre is more represented according to a location? Which genre perform better according à location?
- How do rating and revenue vary as a function of the genre?
- What is the relation between revenues and being awarded
- What is the relationship between ratings and revenues
- Does the cast influence the gender, the revenue amount and the rating?
- What is the optimal runtime for each genre?
- Which relation between the screen time and the opportunity to win an award ?
- Which genre is more nominated/awarded?

## Additional datasets

As we are rating the movies, we need to access the reviews, the budgets, inflation and the oscars awards. We use these additional datasets in order to get our informations:

- Database online: [IMDb free database](https://developer.imdb.com/non-commercial-datasets/) 
- Data scrapping of IMDb reviews (if we have time): [IMDb scores](exploration/IMDb_scrapping_v1.ipynb)
- Data for movie budgets : [TMDB dataset](https://www.kaggle.com/datasets/kakarlaramcharan/tmdb-data-0920)
- Oscars nominations and wins dataset : [Oscars](https://www.kaggle.com/datasets/pushpakhinglaspure/oscar-dataset)
- Dataset used to compute inflation adjusted profits : [US inflation data](https://www.kaggle.com/datasets/varpit94/us-inflation-data-updated-till-may-2021)

## Method

### Part 1: Define the metrics

**Step 1:** We need to define the measures of success. Several indicators could work: number of awards (Oscar, César, etc.), film revenues, reviews, IMDb scores, etc. 

**Step 2:** Since we want to compare films across genres, we need to analyze the distribution of genres across the database. We also need to select which genres to focus on (accroding to the availability of the data).

**Step 3:** We should do the same as the step 2 but for the location. If we keep only the countries, we will have too few data per countries, so we need to define bigger location like mainland: Europe, Asia, Africa, Oceania, America, and USA. 

**Step 4:** We hav to select the other parameters that could be relevant like: 
- Latent personas (from Learning Latent Personas of Film Characters, David Bamman Brendan O’Connor Noah A. Smith): personnas in a successfull action movie will differ from those in a successfull romantic comedy. 
- Language
- Movie runtime
- Famous actors
- Age/gender of actors
- Plot of movies : analyzing popular themes (use NLP to extract a theme for each movie)

### Part 2: Merge & Clean the data

**Step 5:** Load the initial datasets and clean the data. For example we need to have all the date in the same format, we delete the NaN, we clean the textual data and many other things to see in the notebook.

**Step 6:** Classify the genres and the mainland as defined in step 2 and 3. We create two lists, one with the most famous genres and an other with the top 10 genres in the dataset. For the locations we map the country to its mainland (Europe, Asia, Africa, America, Oceania) and we make an exception for the USA because it already represents a huge proportion of the dataset.

**Step 7:** Merge the additional datasets. We can do this thanks to the Wikipedia ID movie and the tconst.

**Step 8:** Check the feasibility of the scientific questions by checking the data availability. For each questions, have we got enough data to answer it? Plot some graphs that can explain/show the feasability.

### Part 3: Analysis

**Step 8:** Answers to scientific questions in response to our problem. This step is key for the analysis because it will highlight the parameters for the best movie according to a specific genre and location.

**Step 9:** Design an easy-to-use interface for the client. The user must be able to select the movie genre and the country where he want to produce the movie, and then we show him the important criteria for a successful film.

## Executed timeline

03.11.2023 : Part 1

**Milestone 2** - 17/11/2023 : Part 2 

10.12.2023 : Step 8

20.12.2023 : Step 9

**Milestone 3** - 22/12/2023 


## Organization within team
| Teammate | Role|
| --- | --- | 
|**Aline** |Initial analysis of scientific questions feasibility|
|**Mathieu**|Data merging and initial analysis of scientific questions feasibility| 
|**Benoit**|Analysis/grouping of genres and countries + ReadMe| 
|**Antoine**|Data cleaning and initial analysis of scientific questions feasibility|
|**Valentin**|Define the formula and the ML algorithm for the success rating |


## Additional ideas

These are some ideas that we wanted to implement, but we need more ressources and time.
- Extract sentiment analysis score of a movie from plot.
- Extract sentiment score of movie reviews and tweets (average, median ?).
- Multiple analysis on the Stanford dataset.





## BAVMA Research Team

This projects takes place in the context of the ADA 2023 course at EPFL Lausanne.

The team members are : 

- Aline Janvier
- Benoît Gallois
- Valentin Parisot
- Mathieu Faure
- Antoine Goupil de Bouillé

