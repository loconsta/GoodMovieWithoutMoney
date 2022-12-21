## Rating, Revenue and Budget

<p align="justify"> The success of a movie is determined by 3 main parameters: its revenue, its budget and its rating. We first analysed the distribtions of these features and their relationship. As such data is scarce, we had to take a subsets of approximately 5'000 movies, which are distributed throughout the years as shown in the figure below: </p>

<center>
  {% include images/year_movie_distr_subset.html %}
</center>


<p align="justify"> The IMDB ratings we worked with are in the range [0,10] where 10 is the maximum and 0 is the minimum, with a mean of 6.5. The distributions of revenue and budget are centred around 100 million US dollars, with a heavy-tailed shape, meaning they are linearly distributed in terms of magnitude (you might see these in logarithm in some plots for this reason). For budget and revenue, it is important to correct the data with monetary inflation in order to be able to compare different years together. Without the monetary correction, there would seem to exist a quite constant increase from 1959 to 2021 in these features, when there are actually none. As can be seen in the figure below, there is higher variability during the first years (1959-1973), which is probably due to the low number of movies during those years compared to more recent years.</p>

<p align="center">
  <img src="images/RRB_across_time.png" />
</p>

<p align="justify"> In both cases (budget, revenue), we see that the median value is below the mean value. It is due to the presence of huge outliers in both variables (heavy-tailed).</p>

<p align="justify"> The third variable, the rating, seems to have on average constantly decreased from the beginning of the timeline (1959) to now, suggesting that it is more difficult to get a high rating now than it was before. This trend might be explained by various factors. It could be that so many movies are available nowadays through various platforms that the public has become more demanding. Another explanation is that the grading community itself might have changed with the advent of internet. A known phenomenon in other areas suggest that bad experiences are more likely to result in a review, and it might have increased with the possibility of grading in a few clicks. Furthermore, some bad old movies may have been forgotten and not included in the databases at all. These are only speculations about the trend; what remains is that it might be harder today to reach a good grade than it was in the past.</p>

<p align="justify"> We analysed how these three variables are correlated; the results are reported in the figure below. As said previously, we used the log of budget and revenue to mitigate the huge domain spammed by these parameters.</p>

<p align="center">
  <img src="images/pairgrid_RRB_by_point.png" />
</p>

<p align="justify">There is a high correlation between the log of budget and the log of revenue, and between the rating and the log of revenue. The surprising (and hopeful for you!) fact is that there is no correlation between the rating and the budget. Even with a low budget, you can imagine producing a film with a high rating, and your rating might (we cannot know at this point) drive revenue. However, budget is still a disadvantage to reach a high revenue.</p>
  
<p align="justify"><i> You lift your head from the paper, your eyes are tired. You feel less stress than before, there is still a chance to get a high rating movie from a low budget. The ratings are getting down with the time, so you realize that you should not be surprised if some people wont love your movie. But which movie type is best suited for this role? You keep reading. </i></p>
