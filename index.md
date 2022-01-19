## Cluster Visualization

Visualising K mean clusters and BDscan Clusters
For my movie recommender I set up an unsupervised machine learning algorithm that will elaborate the initial output and produce movie recommendations as a result. 
I used PCA, K-mean clustering and density based clustering DBscan methods to assess similarity between datapoint, obtaining all in all good results.
The whole thing can be easily be performed without graphical representation, but clarity sake and for me to foster my intuition regarding the solution, I decided to plot the data. I acquired a good understanding of the data corpus and how my clustering captured different aspects of it. 

I initially did a PCA and selected 3 PCs for the graphical representation as those were explain most of the data. You can see a major elbow point at PC 3, meaning that there is  sharp decline in relevance between PC 3 and 4. 

![PCA](https://user-images.githubusercontent.com/45852059/150121693-8d8b575c-ca19-46f4-b9ed-ea059b56838e.png)

As my next step I performed a K-mean clustering, dividing the dataset into 20 clusters. I plotted PC 1 vs 2 and collared the datapoint according to the clusters. 

![cluster1](https://user-images.githubusercontent.com/45852059/150121690-de889ab7-d2b3-446f-9096-f9c561597245.png)

And then did the same with PC 2 vs 3.

![cluster2](https://user-images.githubusercontent.com/45852059/150121689-620addc1-6444-4c14-8780-22501ef12675.png)

Lastly I plotted all 3 PCs in a 3D view to get a better grasp of it. You can tell that the first immagine corresponds to the frontal view, while the second to the view from the bottom.

![cluster 3d](https://user-images.githubusercontent.com/45852059/150121688-e1050230-d3b9-42e3-836d-6bdcd5af76ef.png)

Anyhow the 3D version gives a better understanding of the corpus of the data. It resembles the shape of a pyramid with the point tilted 30° to side. We can also see that the data at the center is much more dense that the one on the outskirts. 


Next I performed a density based clustering. I did this to gather behaviours similarity in the rating behaviour. Basically trying to gather bin addition to the user taste (in the K-mean clustering) also the rating pattern. For this I selected an Epsylon of 0.35 and a minimum samples size of 30. 

I plotted the same graphs so PC 1 vs 2, PC 2 vs 3 and the 3D version. You can tell from the shape that it’s the same size, but the clustering takes a completely different shape. As mentioned before the core has a much higher density and is therefor considered one cluster. The overlaying layer is much less dense and covers the center. In addition we have low significance clusters, due to their small size.

![dbsacn1](https://user-images.githubusercontent.com/45852059/150121686-ca18e9e0-940c-4aec-93c9-5a4ad699119b.png)
![dbsacn2](https://user-images.githubusercontent.com/45852059/150121683-9ce4ec4e-3d27-4205-8dda-1b9d2c3a5a4d.png)
![dbsacn3d](https://user-images.githubusercontent.com/45852059/150121680-e496ed88-97fe-4707-b659-962bceac6cb3.png)

We see how different clustering captures different aspects and leads to completely different results.

To further highlight the difference I plotted the average vote for each movie against the total amount of votes for that movie and collared it by the clusters. As you can see the K-mean capture more similar voted movies while the density clustering captures more movies with similar amount_votes/average_rating movies.

![cluster rating](https://user-images.githubusercontent.com/45852059/150121671-c63263e0-9e0b-4d37-b751-ca7bee4d1f05.png)
![dbscan rating](https://user-images.githubusercontent.com/45852059/150121677-ebad5aa6-2536-41ac-b0e2-5c0195d5a7f8.png)

All in all it was a quiet fun example and I believe the results were quite solid. As we all have different preferences structures, it would be definitely be interesting to capture the user feedback on recommendations to associate to each cluster a weight and therefore relative importance to the other clusters to exploit the cluster classification to a greater extend by recommending movies to the users. 
