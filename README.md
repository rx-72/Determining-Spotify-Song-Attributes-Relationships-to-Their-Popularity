### Determining-Spotify-Song-Attributes-Relationships-to-Their-Popularity

**Joshua Huang**

#### Executive summary

#### Rationale
From a business standpoint, being able to determine specific groupings that correlate to popularity allows Spotify to give better recommendations for users based on said groupings, which would similarly make it more reliable as a music interface and in term more attractive for paying customers. More importantly however, determine the patterns and preferences of users would give people insight on what counts as attractive as music or songs. This would term give greater inspiration to others to explore these fields or perhaps explore less popular fields to showcase how great they can be as songs/music as well.

#### Research Question
The mmain key point we attempt to answer is if we can cluster and organize songs' audio features together in a graphical manner such that we can identify specific hidden groupings and patterns such as song style or genre preferences across the popularity of multiple Spotify songs.

#### Data Sources

The following will be my main source of data:

https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset

It contains a list 114,000 rows of different songs and their popularity from Spotify. Including popularity ranking, each song has 20 columns of features such as artists, album name, energy, key, etc. 

#### Methodology

The main techniques expected to be utilized for this project include data cleaning, feature engineering, pipelining, clustering, and graphing. I expect a lot of cleaning and engineering will be needed to transform the dataset above to a usable state for clustering. Similar, pipelining alone with column transformers will be useful here to aid with the transformation state of the input data. Finally of course, I aim to cluster these features together to see which groups will be focused upon, with some graphing techniques to help visualize these results.

#### Expectations

I expect a large relationship with artists in general for each song, where popularity would be matched with certain artists as well. I also similarly expect certain genres or musical styles to be more popular than others. Aside from this however, I'm not as certain with expected results, as the clustering may come up with some unexpected groupings.

#### Preparation

First a basic eda was performed on the dataset. The head of the dataset was displayed and the dtypes per column were checked before checking on null values which were not found in either the target column ("popularity") nor the features of major interest (energy, key, valence, etc.)

#### Results
(move EDA section to "preparation" above as didn't feel it was fitting with the section)

#### Next steps
What suggestions do you have for next steps?

#### Outline of project

- [Link to notebook 1](https://github.com/rx-72/Determining-Spotify-Song-Attributes-Relationships-to-Their-Popularity/blob/main/EDA.ipynb)
- [Link to notebook 2]()
- [Link to notebook 3]()


##### Contact and Further Information
