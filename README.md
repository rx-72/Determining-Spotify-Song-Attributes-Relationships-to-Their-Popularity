### Determining-Spotify-Song-Attributes-Relationships-to-Their-Popularity

**Joshua Huang**

#### Executive summary

#### Rationale
From a business standpoint, being able to determine specific groupings that correlate to popularity allows Spotify to give better recommendations for users based on said groupings, which would similarly make it more reliable as a music interface and in turn more attractive for paying customers. More importantly however, determining the patterns and preferences of users would give people insight on what counts as attractive as music or songs. This would consequently give greater inspiration to others to explore these fields or perhaps explore less popular fields to showcase how great they can be as songs/music as well.

#### Research Question
The main key point we attempt to answer is if we can cluster and organize songs' audio features together in a graphical manner such that we can identify specific hidden groupings and patterns such as song style or genre preferences across the popularity of multiple Spotify songs.

#### Data Sources

The following will be my main source of data:

https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset

It contains a list 114,000 rows of different songs and their popularity from Spotify. Including popularity ranking, each song has 20 columns of features such as artists, album name, energy, key, etc. 

#### Methodology

The main techniques expected to be utilized for this project include data cleaning, feature engineering, pipelining, clustering, and graphing. I expect a lot of cleaning and engineering will be needed to transform the dataset above to a usable state for clustering. Similar, pipelining alone with column transformers will be useful here to aid with the transformation state of the input data. Finally of course, I aim to cluster these features together to see which groups will be focused upon, with some graphing techniques to help visualize these results.

#### Expectations

I expect a large relationship with artists in general for each song, where popularity would be matched with certain artists as well. I also similarly expect certain genres or musical styles to be more popular than others. Aside from this however, I'm not as certain with expected results, as the clustering may come up with some unexpected groupings.

#### Preparation

First a basic eda was performed on the dataset. The head of the dataset was displayed and the dtypes per column were checked before checking on null values which were not found in either the target column ("popularity") nor the features of major interest (energy, key, valence, etc.). Visualizations of chosen feature variables of interest were then created to examine distribution of variables, correlation to each other, and correlation to the popularity column. These chosen features were:

- danceability
- energy
- valence
- tempo
- loudness
- accousticness

These features were chosen simply because they stood out to me in relation to popularity while also being specific attributes of a song. 

First histograms were ran on each feature to determine their spread and aggregations. Tempo was the most normal distribution bell curve between 0 - 250, followed by valence ranging between 0 - 1.0 (though it had a higher ceiling where most of its bars were large in count). Danceabiltiy was normal but slightly left skewed between 0 - 1.0, and loudness was skewed left between -50 to 0. The most extreme distribution were energy and acousticness, where accoustiness was extremely skewed right and energy was left skewed but bars would constantly increase from 0 to 1.0.

Next we made a heatmap of these features that focused on their correlation with each other. This was to see if certain features may get compounded together if one of them is influential on popularity. Aside from a select few combinations, most correlation tended to be on the lower side and not passing the absolute 0.5 threshold. The main exceptions were energy and loudness at 0.76, energy and acoustiness at -0.73, and loudness and accoustiness at -0.59. These relationships make sense, since high energy resonates with louder music, and high energy and loud music often involves metal or electric music which cuts the naturalness of music accoustiness.

Finally, we made a multi scatterplot where we compared each feature against popularity to determine if there's a trend. No major trend was identifiable with danceability, energy, valence, or tempo. There was a slight trend where larger loudness lead to better popularity and higher accoustiness lead to lower popularity but the values were to spread out to truly make note of this. 

Finally, a basic linear regression model was made to predict popularity using the rest of the dataset features. Each feature was pass through a transformer which, transformed boolean to numerical values, ran a standard scaler on numerical values and a one hot encoder on the categorical values. From there, the train dataset was tranformed and fitted upon before predicting the test dataset. From there, we took the coefficients of the model and see which features were most useful for compatability with popularity. Features with the largest coeffiecent values included:

- time signature
- key
- duration_min

the rest of the features had much lower coefficients utilized on the model. Of course this is a very barebones basic model but we'll keep an eye out for these features during the clustering.

In preparation of the clustering, we run the full dataset under a similar transformation manner as we did with the basic linear regression model, where numerical features were ran under a standard scaler and categorical features were ran under a one hot encoder. The main difference is of course this time the "popularity" column is similar transformed in preparation of clustering. Our final transformed result gives us a dataframe with 114000 rows and 30 columns. Just to recheck, we also have 0 nan values in this frame.

### Dimensional Reductions, Final Steps, and Clustering

Before any next steps, a PCA is ran on the transformed dataset to determine a good sense of how much of the variance is explained by the number of components utilized on the projection of the PCA. In this case, utilizing 2 components explains 33.47% of the projection, a good sign that clustering will work upon here. We also plot the projection no major early groupings and the outliers that exist:

<img src="images/PCA.png" width="500" height="300">

#### Results
(move EDA section to "preparation" above as didn't feel it was fitting with the section)

#### Next steps
What suggestions do you have for next steps?

#### Outline of project

- [Link to notebook 1](https://github.com/rx-72/Determining-Spotify-Song-Attributes-Relationships-to-Their-Popularity/blob/main/EDA.ipynb)
- [Link to notebook 2]()
- [Link to notebook 3]()


##### Contact and Further Information
