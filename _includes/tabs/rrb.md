<p align="justify"> To determine the success of a movie, we want to consider the box office revenue, the budget and the rating. Therefore, we have to analyse the relationship between these features. First of all, we  look at  their distributions:</p>

ADD IMAGE
  
<p align="justify"> The ratings are in the range [0,10] and the distributions of revenue and budget are in logarithmic scale. The last two are centred  around  108 US dollars. We remark that some movies are extremely far away from the centre of the distribution.</p>

<p align="justify"> For budget and revenue, we see that without the monetary correction there is a quite constant increase from 1959 to 2021. We remark that with inflation there is a better stabilisation, meaning that the variable is flatter. There is higher variability during the first years (1959-1973), which are probably due to the low number of movies during those years compared to more recent years.</p>

ADD IMAGE
ADD IMAGE

<p align="justify"> In both cases (budget, revenue), we see that the median value is below the mean value. It is likely that there are huge outliers in both variables. In fact, we can confirm their presence from the distribution plots that we looked before.</p>

<p align="justify"> The budgets and the revenues are corrected by considering the inflation. Thanks to this step we can compare revenues and budgets across years.</p>

<p align="justify"> The third variable, the rating, seems to have on average constantly decreased from the beginning of the timeline (1959) to now. It appears that it is more difficult now to get a high rating than it was before. To understand this mechanism we have to make some reflections. First, nowadays movies are so common that the expectations of a person are higher than in the past. Second, it is way easier to rate a movie with internet connection and social media, this allows people to grade movies directly from home. There is a bias on who rates the movie, if you had a bad experience it is more probable that you share your opinion, even insulting the producer. Instead, it is less probable that you take the time to give a nice and good review. Furthermore, rating on the Internet was less common in the twentieth century. So probably the most popular and appreciated old movies are more often viewed nowadays, and the bad old movies may have been forgotten and not rated. These are just some possible explanations about the trend we remark across the time.</p>

ADD IMAGE

<p align="justify"> Let’s compute the correlation coefficients between the three variables. For all the test statistics we are going to use 5% as a significant threshold. In the plot below we report the correlation coefficient and the p-value for each pairwise comparison. For mitigating the huge domain spanned by the revenue and the budget we use the log scale. We remark that there is a significant correlation between the log of the budget and the log of the revenue, and the rating and the log of revenue. The correlation coefficient for the logarithmic budget-revenue relation is quite high. We can imagine that these two variables share a lot of information. The surprising fact is that there seems to be no correlation between the rating and the budget. Even with a low budget we can imagine producing a film with a high rating.</p>
  
<p align="justify"> You lift your head from the paper, your eyes are tired. You feel less stress than before, there is still a chance to get a high rating movie from a low budget. And you now know that the ratings are getting down with the time, you know that you should not be surprised if not everyone is going to love your movie. But which movie type is best suited for this role? You keep reading.</p>