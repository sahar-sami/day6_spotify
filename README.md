# DAY6 Music Analysis With Spotify
A small data science project to combine practicing my data visualization and machine learning skills with my favorite band, DAY6. DAY6 is a Korean band under JYP Entertainment that has released over 80 songs across multiple albums and EPs. I extracted data from Spotify's Web API using Spotipy to get musical characteristics of every song in the band's discography (excluding multiple versions of the same song) and made some data visualizations as well as performed K-Means Clustering on the data.

## Code and Resources Used
* Python Version 3.7.7
* Python libraries used: numpy, pandas, matplotlib, sklearn, spotipy
* Spotify Web API: https://developer.spotify.com/documentation/web-api/
* Reference article for radar plots in Python: https://python-graph-gallery.com/390-basic-radar-chart/

## Data Collection
Used Spotify's Web API and the Spotipy wrapper library to extract songs from the band and their features. This involved first getting each album, removing albums with repeating songs, retrieving the songs from the remaining albums, and filtering out the last few duplicate songs. Each song had the following features:
* Name
* Album
* Track ID
* Acousticness
* Danceability
* Duration
* Energy
* Instrumentalness
* Key
* Liveness
* Loudness
* Mode
* Speechiness
* Tempo
* Time Signature
* Valence
This dataset is included as "day6.csv" in this repo.

## EDA 
I looked at the distributions of various numerical variables as well as relationships between variables to gain some overall insights of what DAY6's discography is like. These images display some highlights from the EDA. 

## Clustering
I grouped DAY6's songs into 4 clusters using K-Means Clustering. I used the silhouette method to determine that 4 clusters would give me the best results out of the possibility of 3 to 9 clusters. I used PCA (Principal Component Analysis) to visualize the clusters on a 2D graph and radar plots to display the deterministic features of each cluster. 

## Next Steps
* Trying some other clustering algorithms to see if they might produce better results
* Use the clusters as a target variable to classify future releases

