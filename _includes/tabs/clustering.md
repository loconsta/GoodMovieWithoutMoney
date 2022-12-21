
<h2> Clustering </h2>

<p align="justify"> Then, we explored how to separate the data to get meaningful results about how to produce a good movie without much money. First, we expanded our dataset with some new features that were not used before. After that, we manually created some subsets of the data according to the budget and our two measures of success of a movie which are : the average rating and revenue/budget. We wanted to come up with specific attributes of good and cheap movies. </p>

<h3> Separation into groups according to budget and rating </h3>

<p align="justify"> First, we decided to separate the data into high/low budget and high/low rating categories by taking the 0.25 and 0.75 quantiles as cutoff. We looked at the genres reprensentation in the different subsets of the data : </p>

<center>
  {% include images/superposated_radar_charts_genres.html %}
</center>
<br>
The fraction represented in these graphics are over the total number of movies of a particular genre in the whole dataset (5'000).

We remarked that for :
<ul>
  <li> high rating - low budget:  there are many documentaries, western, war movies.</li>
  <li> high rating - high budget: there are many biographies, history movies. There are also several adventure, science-fiction and war movies, but less than the other.</li>
  <li> low rating - high budget: there are many animation, science-fiction, fantasy, family and action movies.</li>
  <li> low rating - low budget subset there are many horror movies. There are also several documentaries, but less than the other.</li>
</ul>

<p align="justify"> We did some statistical tests on the high rating - low budget subset vs the rest of the data on the specific genres that came out. The documentary and war movies are significantly more represented in the low budget - high rating subsets than in the rest of the data. The trend is similar for western, but not significance. </p>

We can do the same representation but with the production countries instead of the genres:

<center>
  {% include images/superposated_radar_charts_countries.html %}
</center>
<br>
We saw that for :
<ul>
  <li> high rating - low budget: there are more movies from DE, DK, ES, HK, KR than in the other subsets. Almost 50% of the movies made in these countries are in this subset. There are also many FR, GB, JP and AU movies. </li>
  <li> high rating - high budget: there are many movies from NZ. </li>
  <li> low rating - high budget: there are many movies from CH. </li>
  <li> low rating - low budget: there are many movies from RU. </li>
</ul>

<p align="justify"> It is interesting to see that in none of the subsets, USA was the major production country. Indeed, the USA produced the majority of the movies in this data set, meaning USA movies have either an average budget or rating. It is more non usual production countries that appear in the subsets of low/high rating and budget. A reason could be that the data are taken from a US based collection, in which foreign movies must be good to be included.</p>

<p align="justify"> Some statistical tests of the data that is high rating - low budget vs all the rest of the data were performed on the specific countries that came out. All the tested countries except JP and AU reached the level of significance. </p>

<p align="justify"> In the subgroup high rating - low budget we looked also at the attributes of the cast members, such the height, the age and the fraction of men. We noticed no difference with the rest of the data. However, when we separated the movies into old and recent ones (cutoff date = 2000), we had some interesting results :</p>

<lu>
  <li> First, we did comparisons inside the high rating - low budget (HR-LB) subsets. There are significantly more women actors in the recent movies from this subset. In addition, there seems to be a tendency in the new movies to have older and shorter actors. </li>

  <li> Then, we compared HR-LB subset with the rest of the data. Before 2000, actors of HR-LB movies are significantly younger. After 2000, the actors are significantly shorter in the HR-LB movies than the others. </li>
</lu>

<h3>Separation into groups according to budget and revenue</h3>

<p align="justify"> Then, we decided to look at our other success measure of the movies which is : revenue/budget. We selected low budget and high revenue/budget movies. First, we looked at the genres representation within this subset : </p>

<center>
  {% include images/single_radar_chart_genres.html %}
</center>
<br>
<p align="justify"> A rapid overview on this subgroup highlights the strong presence of documentaries. There are significantly more documentary, horror and mystery movies in this subset than in the rest of the data. It is interesting to see that this is not exactly the same movie genres that came out from the high rating - low budget subset. </p>

<p align="justify"> We looked at the production countries within this subset and we obtained that there are significantly more movies that are produced in DE, DK, ES and KR in the high revenue/budget - low budget subset than in the rest of the data : </p>

<center>
  {% include images/single_radar_chart_countries.html %}
</center>
<br>
<p align="justify"> By performing again a cast analysis, we compared this subset with the rest of the data. We could draw the same conclusions as for the comparison of the actor attributes of the high rating - low budget subset and the rest of the data. However, we observed significantly more women actors in recent high revenue/budget - low budget movies compare to the rest of the data. It was just a tendency in the high rating - low budget subset. </p>