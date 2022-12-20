<p align="justify"> To determine the success of a movie, we want to consider the box office revenue, the budget and the rating. Therefore, we have to analyse the relationship between these features. First of all, we  look at  their distributions:</p>

<p align="center">
  <img src="images/hist_RRB_log.png" />
</p>
  
<p align="justify"> The ratings are in the range [0,10] where 10 is the maximum and 0 is the minimum. The distributions of revenue and budget are in logarithmic scale. The last two are centred  around  100 million US dollars. We remark that some movies are extremely far away from the centre of the distribution.</p>

<p align="justify"> For budget and revenue, it is important to correct the data with monetary inflation in order to be able to compare different years together. The inflation coefficient available starts from 1959 until now. As expected without the monetary correction there is a quite constant increase from 1959 to 2021 in revenue and budget. The inflation is able to stabilize the values. There is higher variability during the first years (1959-1973), which is probably due to the low number of movies during those years compared to more recent years.</p>

<p align="center">
  <img src="images/RRB_across_time.png" />
</p>

<p align="justify"> In both cases (budget, revenue), we see that the median value is below the mean value. It is likely that there are huge outliers in both variables. In fact, we can confirm their presence from the distribution plots that we looked at before.</p>

<p align="justify"> The third variable, the rating, seems to have on average constantly decreased from the beginning of the timeline (1959) to now. It appears that it is more difficult now to get a high rating than it was before. To understand this mechanism we have to make some futher considerations. First, nowadays movies are so common that the expectations of a person are higher than in the past. Second, it is way easier to rate a movie with internet connection and social media, this allows people to grade movies directly from home. There is a bias on who rates the movie, if you had a bad experience it is more probable that you share your opinion, even insulting the producer. Instead, it is less probable that you take the time to give a nice and good review. Furthermore, rating on the Internet was less common in the twentieth century. So probably the most popular and appreciated old movies are more often viewed nowadays, and the bad old movies may have been forgotten and not rated. These are just some of the possible explanations about the trend we remark across the time.</p>

<p align="justify"> We compute the correlation coefficients between the three variables. For all the test statistics we are going to use 5% as a significant threshold. In the plot below we report the correlation coefficient and the p-value for each pairwise comparison. For mitigating the huge domain spanned by the revenue and the budget we use the log scale. We remark that there is a significant correlation between the log of the budget and the log of the revenue, and the rating and the log of revenue. The correlation coefficient for the logarithmic budget-revenue relation is quite high. We can imagine that these two variables share a lot of information. The surprising fact is that there is no correlation between the rating and the budget. Even with a low budget we can imagine to produce a film with a high rating.</p>

<p align="center">
  <img src="images/pairgrid_RRB_by_point.png" />
</p>
  
<p align="justify"> You lift your head from the paper, your eyes are tired. You feel less stress than before, there is still a chance to get a high rating movie from a low budget. The ratings are getting down with the time, so you realize that you should not be surprised if some people wont love your movie. But which movie type is best suited for this role? You keep reading.</p>
