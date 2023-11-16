How to achieve glory and success

## Datastory

A producer comes to see us and wants to make a successfull movie in a given genre and for a geographical-area. He wants to find the best drivers that will make his movie sucessfull. We decided to create an easy-to-use interface where the producer can select his parameters and find a way to make the film that will bring him fame and success. 

You can access the interface by clicking on the link: [Interface](Mettre un lien vers une page web qui dit :"interface en construction")


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

As we are rating the movies, we need to access the reviews and the oscars awards and nominations. We use these additional datasets in order to get our informations:

- Database online: [IMDb free database](https://developer.imdb.com/non-commercial-datasets/) 
- Data scrapping of IMDb reviews (if we have time): [IMDb scores](exploration/IMDb_scrapping_v1.ipynb) 
** A COMPLETER **

## Method

### Part 1: Define the metrics

**Step 1:** We need to define the **measures of success**. Several indicators could work: number of awards (Oscar, César, etc.), film revenues, reviews, IMDb scores, Twitter/X reactions, etc. 

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



## Questions and analysis

### Measures of success:  

| Measure | Advantages | Disadvantages | Sources|
| --- | --- | --- | --- |
|**Price and nominations** |Reliability |Price are not the same. Hard-to-find information | Scrapping Internet or Wikipedia|
|**Box-office revenue**| Numerical value |Depends on the country, depends on the budget invested. Better to find the return on investment | Difficult to find |
|**Movie reviews**| Using NLP, sentimental analysis| Subjective| Available on IMDb |
|**IMDb number of votes**| Adds credibility to the ratings, objective|Not a always correlated with success |Scrapping of IMDb website |
|**IMDb ratings**|Objective | Difficult to access for all movies| Scrapping of IMDb website|
|**Twitter/X reactions**|Sentimental analysis|Only available for recent movies|Using Twitter Api and find reactions to #movie_name|

### Questions and first comments

1) How do rating and revenue vary as a function of genre : XXX

2) XXX

3) XXX



## Further steps and methodology

### 1. Finding data and cleaning
IMDb: 
- Database online: [IMDb free database](https://developer.imdb.com/non-commercial-datasets/) 
- Data scrapping of IMDb reviews (if we have time): [IMDb scores](exploration/IMDb_scrapping_v1.ipynb) 

Twitter:
- Twitter API (if we have time): extract tweets for each modern movie

Awards:
- Finding nominations for main movie festivals: try to scrap the data for main festivals
-  

Cleaning CMU database:


Merging dataframes:
- Merging CMU movies dataframe with IMDb ratings




### 2. NLP 
- Extract themes from movie plots: find key words linked to movie genre ? 
- Extract sentiment analysis score of a movie from plot 
- Extract sentiment score of movie reviews and tweets (average, median ?)

### 3. Defining success scores based on sucess measures
- Give a score for each award 
- Find a formula for a general scoring based on all measures 

### 4. Vizualization of data and correlations
- Show correlation matrix
- Interesting plots
- Heatmap sentimental analysis over years and genre

### 5. Modeling using regressions / ML algorithms 
- Revenue brought for each actor in the cast: linear regression with categorical data: show best actors

### 6. Analyzing results
- Showing most relevant topics for each genre and period

### 7. Create an interface to vizualize results for each segmentation
- Streamlit interface / website that displays the main graphs for each segment : period + genre


## GANT graph

METTRE UN GANT POUR EXPLIQUER QUI FAIT QUOI JUSQUA LA FIN

## Data set 

- [CMU Movie Summary Corpus](README_dataset.md): 42,306 movie plot summaries extracted from Wikipedia + aligned metadata extracted from Freebase, including: 1) Movie box office revenue, genre, release date, runtime, and language, 2) Character names and aligned information about the actors who portray them, including gender and estimated age at the time of the movie's release
- [Stanford CoreNLP-processed summaries](http://www.cs.cmu.edu/~ark/personas/data/corenlp_plot_summaries.tar) : All of the plot summaries from above, run through the Stanford CoreNLP pipeline (tagging, parsing, NER and coref).


## Graphs 

### Historical periods
![MOVIES ACCORDING TO TIME](exploration/figures/movies_release_date2.png)

### Film genres
![MOVIES GENRES REPARTITION](exploration/figures/movies_genres2.png)

### Language repartition
![MOVIES LANGUAGES REPARTITION](exploration/figures/movies_language2.png)


## Sources

- [IMDb ratings scrapping](https://www.geeksforgeeks.org/scrape-imdb-movie-rating-and-details-using-python/)
- Learning Latent Personas of Film Characters, David Bamman Brendan O’Connor Noah A. Smith
- [NLP for movie history on medium](https://towardsdatascience.com/an-nlp-movie-history-44487ec0144f)
- [Festival nomination website](https://mfdb.eu/en/): easy to scrap


## Packages 

- Front-end : Streamlit 
- Data analysis and plots : Sns, Matplotlib, Pandas, Numpy
- Scrapping : bs4, request 


Use the package manager [pip](https://pip.pypa.io/en/stable/) to install packages
```bash
pip install pandas
```

## BAVMA Team

This projects takes place in the context of the ADA 2023 course at EPFL Lausanne.

The team members are : 

- Aline Janvier
- Benoît Gallois
- Valentin Parisot
- Mathieu Faure
- Antoine Goupil de Bouillé

