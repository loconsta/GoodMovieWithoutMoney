### Clustering

<p align="justify"> Then we will explore how to separate the data to get meaningful results about how to produce a good movie without many money. First, we expanded our dataset with some new features that were not used before. After that, we manually created some subsets of the data according to the budget and our two measures of success of a movie which are : the average rating and $\frac{revenue}{budget}$. We would like to be able to come up with specific attributes of good and cheap movies. </p>


#### Separation into groups according to budget and rating

<p align="justify"> First, we decided to separate the data into high/low budget and high/low rating categories. We took the 0.25 and 0.75 quantiles as cutoff. We looked at the genres reprensentation in the different subsets of the data : </p>

<center>
  {% include images/superposated_radar_charts_genres.html %}
</center>
  
We can remark that for :

* high rating - low budget:  there are more documentaries, western, war movies.
* high rating - high budget: there are more biographies, history movies. There are also several adventure, sci-fi and war movies, but less than the other.
* low rating - high budget: there are more animation, scifi, fantasy, family and action movies.
* low rating - low budget subset there are more horror. There are also several documentaries, but less than the other.

<p align="justify"> We did some statistical tests on the high rating - low budget subset vs the rest of the data on the specific genres that came out. The documentary and war movies are significantly greater in the low budget - high rating subsets than in the rest of the data. For Western, we did not reach the level of significance. </p>

We can do the same representation but with the production countries instead of the genres:

<center>
  {% include images/superposated_radar_charts_countries.html %}
</center>

We can see that for :

* high rating - low budget: there are more movies from DE, DK, ES, HK, KR than in the other subsets. The fraction around 0.5 so, it means that nearly the majority of movies of the whole data set are contained in this subset. There are also many FR, GB, JP and AU movies in this subset.
* high rating - high budget: subset there are more movies from NZ.
* low rating - high budget: subset there are more movies from CH.
* low rating - low budget: subset there are more movies from RU.

<p align="justify"> It is interesting to see that in none of the subsets, USA was the major production country. Indeed, the USA produced the majority of the movies in this data set. So, it means that the USA produced movies that have an average budget or rating. It is more non usual production countries that appeared in the subsets of low/high rating and budget. A reson of this could be that the data are taken from a US based collection, in which foreign movies must be good in order to be included.</p>

<p align="justify"> Let's do some statistical tests of the data that is high rating - low budget vs all the rest of the data on the specific countries that came out. All the tested countries except JP and AU reached the level of significance. </p>

<p align="justify"> In the subgroup high rating - low budget we looked also at the attributes of the cast members, such the height, the age and the fraction of men. We noticed no difference with the rest of the data. However, when we separated the movies into old and recent ones (cutoff date = 2000), we had some interesting results :</p>

* First, we did comparisons inside the high rating - low budget (HR-LB) subsets. There are significantly more women actors in this subset. It seems to have a tendency in the new movies to have older and shorter actors within this subset

* Then, we compared HR-LB subset with the rest of the data. Before 2000, actors of HR-LB movies were significantly younger. After 2000, the actors are significantly shorter in the HR-LB movies than the others. 


#### Separation into groups according to budget and revenue 

<p align="justify"> Then, we decided to look at another success measure of the movies which is : $\frac{revenue}{budget}$. So, we selected low budget and high $\frac{revenue}{budget}$) movies. First, we looked at the genres representation within this subset : </p>

<center>
  {% include images/single_radar_chart_genres.html %}
</center>
  
<p align="justify"> A rapid overview on this subgroup highlights the strong presence of documentaries. There are significantly more documentary, horror and mystery movies in this subset than in the rest of the data. It is interesting to see that this is not exactly the same movie genre that came out from the high rating - low budget subset. </p>

We looked at the production countries within this subset and we obtained that there are significantly more movies that are produced in DE, DK, ES and KR in the high $\frac{revenue}{budget}$ - low budget subset than in the rest of the data :

<center>
  {% include images/single_radar_chart_countries.html %}
</center>

<p align="justify"> By performing the cast analysis, we compared this subset with the rest of the data. We could draw the same conclusions as for the comparison of the actor attributes of the high rating - low budget subset and the rest of the data except that we observed significantly more women actors in recent high $\frac{revenue}{budget}$ - low budget movies compare to the rest of the data. It was just a tendency in the high rating - low budget subset. </p>
