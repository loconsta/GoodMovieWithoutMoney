We are going to bring you on an amazing journey inside the Hollywood world. Enjoy the reading.

<p align="justify"> Please, pretend to be an emerging movie director. You are young with no experience at all, but you studied hard at the renowned Action-Drama Academy, commonly known as ADA, and you want to prove your abilities, because as your mama says you are the best person in the world. You have just finished the last exam. That night you get drunk with your friends, you are celebrating your achievement. Your phone rings. An agent from Hollywood is calling you. You are too high to really understand what is happening, the only neuron that is left says: “Probably it is just a fake call”. Therefore, you pretend to be the best student in all the history of the world. </p>

<p align="justify"> You wake up, it is 2 p.m. and you have no memory of the night before. Suddenly, a message arrives: “Thank you for the nice talk, as we discussed yesterday you have 1 year to propose and produce a great movie. Your budget is …  and you are free to make whatever choice you want. Good look.”</p>

<p align="justify"> Now that all of your neurons are awake you understand the big problem you have: you are asked to produce a movie and of course you have a limited budget, otherwise it would have been too easy, and as you know life is not easy. You know that if you miss this chance all of your hard work at the academy is going to be wasted. It is time for big responsibilities. Do you want to make a difference in the history of film?</p>

<p align="justify"> You have no idea where to start, there are so many different kinds of movies. Which one will bring you success? During your studies someone told you that there is a consulting company that helps young directors to reach fame after graduation. You look through your stuff, the business card is still there:</p>

<p align="center">
  <img src="images/card.jpg" />
</p>

<p align="justify"> You immediately send an email to Mr. Costantin. You receive a fast answer, which is already a good sign. You schedule a meeting with the boss of the NoLemonNoMelon company in a few days. The only thing you need to do is to wait.</p>

<p align="justify"> The day has come, 2 minutes before the meeting time you click on the zoom link Loris gave you. Of course, you haven’t updated zoom, now you have to wait. At the end you only have 1 minute of delay. During the discussion you and Mr. Costantin make a deal: he is going to collect and analyse all the movie data he finds in order to provide you with the kind of movie you should produce. In exchange you will pay him 5% of your revenue.</p>

Mr. Costantin and his amazing team work day and night to present the analysis as soon as possible.

After 2 weeks you receive an envelope with the results from the consulting company you hired.

## Letter
  
Dear future movie director,

Me and my team worked full-time to provide you this report. We hope you are going to appreciate the analysis we made. 

We stay at your disposal for any additional questions.

Best regards,

Loris Costantin


## Abstract

<p align="justify"> In the late 19th century the entertainment industry saw the advent of the first films. In the past hundred years movies have become an integral part of the lives of people around the globe. Nowadays, the movie industry has seen the advent of "superproductions" supported by insane amounts of money. However, budget might not be a mandatory prerequisite for movie quality, appreciation and revenue. We aim to study the relationship between movie rating, revenue, and budget throughout the last 60 years. In addition, we want to include movie genres in our analysis, and hope to reveal a time-dependent effect of trends in the movie industry. This would be signalled by an increased revenue/rating due only to genre differences, changing across decades. Lastly, we are interested in low budget movies with high revenue and ratings. We want to investigate possible common characteristics of these movies and how they evolve with time. </p>

## Datasets
A huge collection of movies for the past century and the beginning of this century. A [CMU Movie Summary Corpus](http://www.cs.cmu.edu/~ark/personas/) served as our base dataset. To enable a complete overview of the movie distribution, we completed it using data from [IMDB](https://datasets.imdbws.com/), [TMDB](https://developers.themoviedb.org/3/getting-started/introduction), [Wikipedia](https://www.wikipedia.org/) and corrected monetary values using [inflation data](https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG). The next figure gives an idea of the number of movies in each year that are contained in the database used for the analysis.The number of films produced in the twenty-first century has skyrocketed, exceeding 10,000 per year.

<p align="center">
  {% include year_movie_distr.html %}
</p>

## Results

### Exploratory analysis

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
  


### Genre analysis
  
<p align="justify"> We now want to focus on genre. In the next plot we want to give an idea of the different genres present in the data set. Below we display the genres present in the dataset. We remark that drama, documentary and comedy movies are extremely present compared to other categories such as thriller movies. We have to keep this into account when we do our analysis. </p>
  
ADD IMAGE
  
  
We explore our three variables, rating, budget and revenue, for each genre:
  
ADD IMAGE 
  
<p align="justify"> From these representations we remark that genres with highest rating are in order: biography, western and war. Biography movies have a significantly higher rating than the others, except for western and war films. Concerning the revenue, the highest is obtained by the adventure category and the lowest with documentaries. This last category has a lower budget and revenue than the others.</p>
  
<p align="justify">Until now, the analyses have covered the entire time period from 1959 to 2021. Now, it would be interesting to understand how genres evolve over time. A general decrease in rating score was perceived in a first analysis. Is it the case for all movie’s genre, and is this decrease significant? The movies are then divided into two periods, with 2000 as the cut-off point, when an increase in the number of movies is observed. The next figure reports the results on rating, revenue and budget, before and after the cut-off.</p>
  
ADD IMAGE
  
<p align="justify"> Romance, mystery, horror, history, documentary, comedy, biography, and animation movies were significantly better rated before 2000. Action movies and science-fiction show a (non-significant)  increase in rating score. All the other categories display a non-significant decrease of the average rating score. This makes the analysis more complicated.  The trend is similar for all genres, the ratings are decreasing.</p>
  
<p align="justify"> No movies show significant increase in their revenue, whereas romance, history, drama, crime, comedy, and biography movies have a significant decrease.</p>

<p align="justify"> Science fiction, adventure, and action movies show a significant increase in budget, whereas romance and drama movies undergo a significant decrease in their budget. </p>

<p align="justify"> Thus, a significant increase in budget (such as for action, adventure, and science fiction movies) does not reflect a significant increase in the revenue.</p>

<p align="justify"> In the second period, it seems harder to create movies as good as in the past. This could be due to the increasing concurrence. </p>


### Clustering
  
<p align="justify"> Let’s perform a deeper analysis. We are considering clusters of pairwise rating, budget and revenue in low and high space. With the representation below, we report the fraction of movies over the total number of movies of a particular genre in the whole dataset. It is why the fractions are small, because the 4 groups do not contain a lot of data points. </p>

  
ADD IMAGE
  

We can remark that for :

* high rating - low budget:  there are more documentaries, western, war movies.
* high rating - high budget: there are more biographies, history movies. There are also several adventure, sci-fi and war movies, but less than the other.
* low rating - high budget: there are more animation, scifi, fantasy, family and action movies.
* low rating - low budget subset there are more horror. There are also several documentaries, but less than the other.

<p align="justify"> We did some statistical tests on the high rating - low budget subset vs the rest of the data on the specific genres that came out. We used an independent t-test as there are not the same amount of movies in the different data sets that are compared. The documentary and war movies are significantly greater in the low budget - high rating subsets than in the rest of the data. For Western, we did not reach the level of significance. </p>



We can do the same representation but with the countries instead of the genres:

ADD IMAGE

We can see that for :

* high rating - low budget: there are more movies from DE, DK, ES, HK, KR than in the other subsets. The fraction around 0.5 so, it means that nearly the majority of movies of the whole data set are contained in this subset. There are also many FR, GB, JP and AU movies in this subset.
* high rating - high: subset there are more movies from NZ.
* low rating - high: subset there are more movies from CH.
*vlow rating - low: subset there are more movies from RU.

<p align="justify">It is interesting to see that in none of the subsets, the major production country of the whole data set (USA) has no peak. Indeed, the USA produced the majority of the movies in this data set. So, it means that the USA produced movies that have an average budget or rating. It is more non usual production countries that appeared in the subsets of low/high rating and budget.</p>

We can see that DE, DK, ES, HK, KR has a good potential to produce cheap and good movies.

<p align="justify"> Let's do some statistical tests of the data that is high rating - low budget vs all the rest of the data on the specific countries that came out. All the tested countries except JP and AU reached the level of significance. </p>

<p align="justify"> In the subgroup high rating - low budget we can more carefully look at the attributes of the cast members, such the height, the age and the fraction of men. In the next figure we display the result of the cast analysis while we take into consideration the recent movies and the old movies, using 2000 as cut-off year.</p>

ADD IMAGE

Comparison inside the high rating - low budget (HR-LB) movies :

* There are significantly more women actors in the new movies (fraction of men is lower).
* It seems to have a tendency in the new movies to have older and smaller actors.

Comparison inside the rest of the movies :

* The actors are now significantly younger than before
* There are significantly more female actors in the new movies (fraction of men is lower).

Comparison between HR-LB movies and the rest of the data :

* Before 2000, actors of HR-LB movies were significantly younger
* After 2000, the actors are significantly smaller in the HR-LB movies than the others.


<p align="justify"> It is time to focus on the revenue instead of the rating. We can take into account the ratio between revenue and budget as a measure of the success instead of the rating. Of course we also select a low budget, which reflects the situation in which we are.</p>
  
ADD IMAGE
  
<p align="justify"> A rapid overview on this subgroup highlights the strong presence of documentaries. There are significantly more documentary, horror and mystery movies in this subset than in the rest of the data. It is interesting to see that this is not exactly the same movie genre that came out from the high rating - low budget subset, were documentary and war movies that were significant.</p>

We can perform the same analysis in space instead of in the genre categories and we obtains that there are significantly more movies that are produced in DE, DK, ES and KR in the high revenue/budget - low budget subset than in the rest of the data:

ADD IMAGE


<p align="justify"> By performing the cast analysis as before we can draw the same conclusions as for the comparison of the actor attributes of the high rating - low budget subset and the rest of the data except for the fraction of men. Here, we observe that there are significantly more women actors in recent and old movies in the subset, compared to the rest of the data. Moreover, we have also more women actors in recent movies than older ones as for the high rating - low budget subset.</p>

ADD IMAGE

### Conclusion

<p align="justify"> Concerning the genre of the movie, documentary, horror, mystery, and war movies are good opportunities. If you want to earn money and also have a good rating with a low budget, you should concentrate only on documentaries. If your goal is to earn money with a low budget, documentary, horror, and mystery genres are the best. Finally, if you want to have a good rating with a low budget, documentary and war movies are the best.</p>
<p align="justify"> Concerning the production countries, Germany, Danemark, Espagne, Hong Kong, South Korea, France, and Great Britain are good opportunities. If you want to earn money and also have a good rating with a low budget, you should concentrate only on Germany, Danemark, Espagne, and South Korea.</p>
<p align="justify"> Concerning the actors' attributes, nothing comes out without the separation into old and recent movies. So, now, you should take your cast with an average age between 36 and 39 years, of a height of around 1.74m. Your cast should also have a fraction of men actors around 0.63 that have a tendency to reduce throughout the years.</p>


<p align="justify"> With the result presented in this report we suggest you to focus on documentaries for getting high ratings with low budgets. The revenue you can get is not extremely high but you can still easily earn 10 times the given budget. Another strong point for the documentary is that you are not required to select a cast because nature is outside just for you, ready to become a movie star. </p>



<p align="justify"> You have finished reading the report. You take a deep breath. You look outside the window and your eyes shine. The world is full of amazing creatures, views and diversity. You are going to produce a documentary that everyone is going to remember.</p>



<p align="center">
  <img src="images/test_monkey.jpg" />
</p>

We are currently trying to create this website. If you see a bunch of nice monkeys above, we are on track to get this thing done, so Cheers !!
