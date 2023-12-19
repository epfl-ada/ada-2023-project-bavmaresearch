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
