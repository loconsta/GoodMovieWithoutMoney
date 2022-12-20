<p align="justify"> Let’s perform a deeper analysis. We are considering clusters of pairwise rating, budget and revenue with low and high values. With the representation below, we report the fraction of movies over the total number of movies of a particular genre in the whole dataset. It is why the fractions are small, because the 4 groups do not contain a lot of data points. </p>


<center>
  {% include images/radarChartGenres.html %}
</center>
  
We can remark that for :

* high rating - low budget:  there are more documentaries, western, war movies.
* high rating - high budget: there are more biographies, history movies. There are also several adventure, sci-fi and war movies, but less than the other.
* low rating - high budget: there are more animation, scifi, fantasy, family and action movies.
* low rating - low budget subset there are more horror. There are also several documentaries, but less than the other.

<p align="justify"> We did some statistical tests on the high rating - low budget subset vs the rest of the data on the specific genres that came out. We used an independent t-test as there are not the same amount of movies in the different data sets that are compared. The documentary and war movies are significantly greater in the low budget - high rating subsets than in the rest of the data. For Western, we did not reach the level of significance. </p>

We can do the same representation but with the countries instead of the genres:

<center>
  {% include images/radarChartCountries.html %}
</center>

We can see that for :

* high rating - low budget: there are more movies from DE, DK, ES, HK, KR than in the other subsets. The fraction around 0.5 so, it means that nearly the majority of movies of the whole data set are contained in this subset. There are also many FR, GB, JP and AU movies in this subset.
* high rating - high budget: subset there are more movies from NZ.
* low rating - high budget: subset there are more movies from CH.
* low rating - low budget: subset there are more movies from RU.

<p align="justify">It is interesting to see that in none of the subsets, USA was the major production country. Indeed, the USA produced the majority of the movies in this data set. So, it means that the USA produced movies that have an average budget or rating. It is more non usual production countries that appeared in the subsets of low/high rating and budget. A reson of this could be that the data are taken from a US based collection, in which foreign movies must be good in order to be included.</p>

We can see that DE, DK, ES, HK, KR has a good potential to produce cheap and good movies.

<p align="justify"> Let's do some statistical tests of the data that is high rating - low budget vs all the rest of the data on the specific countries that came out. All the tested countries except JP and AU reached the level of significance. </p>

<p align="justify"> In the subgroup high rating - low budget we can more carefully look at the attributes of the cast members, such the height, the age and the fraction of men. Here there is the result of the cast analysis while we take into consideration the recent movies and the old movies, using 2000 as cut-off year.</p>

Comparison inside the high rating - low budget (HR-LB) movies :

* There are significantly more women actors in the new movies (fraction of men is lower).
* It seems to have a tendency in the new movies to have older and shorter actors.

Comparison inside the rest of the movies :

* The actors are now significantly younger than before
* There are significantly more female actors in the new movies (fraction of men is lower).

Comparison between HR-LB movies and the rest of the data :

* Before 2000, actors of HR-LB movies were significantly younger
* After 2000, the actors are significantly shorter in the HR-LB movies than the others.

<p align="justify"> It is time to focus on the revenue instead of the rating. We can take into account the ratio between revenue and budget as a measure of the success instead of the rating. Of course we also select a low budget, which reflects the situation in which we are.</p>
  
<center>
  {% include images/singleRadarChartGenre.html %}
</center>
  
<p align="justify"> A rapid overview on this subgroup highlights the strong presence of documentaries. There are significantly more documentary, horror and mystery movies in this subset than in the rest of the data. It is interesting to see that this is not exactly the same movie genre that came out from the high rating - low budget subset, were documentary and war movies that were significant.</p>

We can perform the same analysis in space instead of in the genre categories and we obtains that there are significantly more movies that are produced in DE, DK, ES and KR in the high revenue/budget - low budget subset than in the rest of the data:

<center>
  {% include images/singleRadarChartCountry.html %}
</center>

<p align="justify"> By performing the cast analysis as before we can draw the same conclusions as for the comparison of the actor attributes of the high rating - low budget subset and the rest of the data except for the fraction of men. Here, we observe that there are significantly more women actors in recent and old movies in the subset, compared to the rest of the data. Moreover, we have also more women actors in recent movies than older ones as for the high rating - low budget subset.</p>
