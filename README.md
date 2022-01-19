# Unsupervised-Movie-Recommender
An unsupervides learning based movie recommender performed with PCA, K-Mean and DBSCAN Clustering.
It also cosists of a lot of merging and joining of databases. So much that I thougt to rename it either: **"Fun with Pandas"** or **"Fun with MERG".**

### Unsupervised Movie Recommender 


Intro.
This project uses unsupervised learning to generate movie recommendations. It cross validates user behaviour and rating of movies based on an initial input of 3 liked movies. 

Object
Since every user might have a different value structure and comparison portfolio, comparing strictly the rating of a movie does not lead to good suggestions. Me personally, I struggle on the general streaming platforms (ie. Netflix) to find movies I like. At the same time, from my experience, I tend to rely much more on specific individuals (friends) or some critic website (rotten Tomatoes) to advice me for good movies to watch. These recommendations are usually not blog buster movies, don’t have crazy action scenes in them and tend to be of the indi genere. At the same time I love myself some pulp classics like Fight Club, I am a big fan of the Italian director Fellini and will quite always say yes to a night with friends watching some high quality trash. All in all, I can’t say, I can clearly identify the right patterns for my movie recommender. But maybe ML can! Therefor I developed the rough outline of a movie recommender that is based rather on other user behaviour rather than on the general opinion.

Method

I started with some data engineering and Pandas Magic to get the database I needed and went  on to perform some clustering and PCA analysis. Arguably I could have perform Factor Analysis as well, but really think it is overkill at this time ( ie. unnecessary) and think that implanting more functionalities, maybe a future feedback function and a user-friendly interface would be of greater importance. I decided to completely ignore the genere of the movies, since I wanted to give the user behaviour an increased importance and also because, I don’t feel like the genere changes my willingness to see a movie or not.

Outcome

Quite impressive. The initial input movies were:

Next Steps
 
Next steps would be to use a bigger database, create an interface and increase in flexibility the input function. It would also be quite interesting for the user to input not only the movies he/she liked, but also the rating associated. Therefore I could state not only my favourite movies, but also movies that I thought were average or utterly disgraceful. A further expansion of the database with additional info regarding the movies would also be interesting, linking the year, the numbers of views, prices won, budget spent, director and cast. 



