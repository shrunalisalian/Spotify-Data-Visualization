# Spotify-Data-Visualization

My teammates and I worked on the Spotify's dataset available on Kaggle. You can download the dataset here https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-19212020-600k-tracks
This is a Data Visualization project in R. Spotify was the first legal online streaming platform for music. It was founded in 2006 and till date owns the 
largest consumer share compared to its competitors. 
We have divided the project into 3 domains.
1) Trend Analysis
2) Feature Analysis
3) Time Series Analysis

There are a total of 12 visualizations, four in each category. 
1) Trend Analysis 
a) Spotify's Performance over the years 
The number of tracks uploaded on Spotify for each year has been consistently increasing. In 2013 we see a more than regular increase in the number of 
tracks being uploaded and the reason is, the prices of compact disc began to increase during the same time frame. This was combined with the growing 
popularity of streaming platforms.
Next we saw a drop in the number of tracks uploaded for the first time in 2017. The reason for this is unclear. However, from what we know, Spotify went public 
in 2018 and recorded the largest ever operational costs in its history in 2017 due to worldwide expansion. 

b) Covid Hypothesis
Music and mental health have a direct correlation - https://twitter.com/mshannahmurphy/status/1238380534075494401
Since in businesses demand and supply go hand-in-hand. We hypothesized that during covid artists might release more happy or sad songs. In other words,
we were hoping to see a change in the type of tracks released during covid versus before. But our hypothesis proved wrong. We saw no change in the type of 
tracks released on Spotify.

c) Deciding factors for the popularity of a track on Spotify
After analysing the correlation between different metrics, we understood that track popularity is majorly driven by an artist's popularity which in turn is 
driven by his/her followers. No other factor majorly influences the popularity of a track. 

2) Feature Analysis
a)How are features of a song related to one another
We see a significant correlation between 
  i) valence -  energy
  ii) valence - danceability
  iii) valence - loudness
  iv) loudness - energy
  
b) Energy - Loudness
The track loudness and energy are directly proportional. 

c) What factors contribute to the tracks popularity for a popular artist?
Track characteristics do not play a significant role in determining the popularity of an artist’s tracks.

d) Popular tracks of a leading artist
Word cloud visualization indicates that the track titles “hold_on” and “anyone” appear frequently for the artist Justin Bieber. 

e) What variation in track characteristics can be observed across the top 10 music genres?
The “kleine hoerspie” genre possesses the highest values for several track features, including “track_danceability,” “track_energy,” “track_key” ,
“track_loudness,” “track_mode,” “track_speechiness,” and “track_acousticness.” This allows us to observe the variations in each track characteristic among 
the top 10 music genres.

3) Time Series Analysis
a) What is the inclination of Spotify users towards particular artists, and does the year of release play a role in shaping these preferences?
The plot also shows an increase in popularity for artists in more recent years compared to those in the early ones.This could be due to a few different 
factors such as the evolution of the music industry in terms of genre preferences, better technology used to create music, globalization of popular 
genres, etc.

b) What is the inclination of Spotify users towards different genres of music? Does the decade that this genre originated have an impact on whether people
still listen to it?
the top 5 genres by popularity that originated in each decade between 1920-2020. What is interesting to note is that the most popular genres of all 
time on Spotify are those that originated in the 2000s. From the previous plot(PLOT1), we saw that artists of older decades did not fare well in terms of 
popularity, but the same trend does not apply to genres. This shows that artists of recent years have adapted older genres into their style of music to 
make it more appealing to the audience.

c) What is the popular attitude towards explicit content in music?
The mean in this case would represent the proportion of 1s (explicit) in the data set. So, for a given decade, if the mean of the explicitness variable 
is 0.6, this would mean that 60% of the tracks in the data set for that decade are explicit. By aggregating the mean explicitness per decade, we can see 
how the proportion of explicit tracks has changed over time and whether there are any trends or shifts in attitudes towards explicit content.This shows 
us that the cultural attitude towards explicit music and an artist’s freedom of expression has increased largely, with most popular songs in the recent 
decades of the 2000s having popular tracks with explicit lyrics.
