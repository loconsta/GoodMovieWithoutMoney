<p align="justify"> We now want to focus on genre. In the next plot we want to give an idea of the different genres present in the data set. Below we display the genres present in the dataset. We remark that drama, documentary and comedy movies are extremely present compared to other categories such as thriller movies. We have to keep this into account when we do our analysis. </p>
  
<center>
  {% include images/overall_genre_distr.html %}
</center>
  
We explore our three variables, rating, budget and revenue, for each genre:
  
<p align="center">
  <img src="images/RRB_genre_CIs.png" />
</p>
  
<p align="justify"> From these representations we remark that genres with highest rating are in order: biography, western and war. Biography movies have a significantly higher rating than the others, except for western and war films. Concerning the revenue, the highest is obtained by the adventure category and the lowest with documentaries. This last category has a lower budget and revenue than the others.</p>

<p align="justify"> Another value which would be interesting to look at is what we can call rentability: the ratio between revenue and budget. In fact a high revenue alone does not tell us a lot of information, it is better to understand how many times the revenue is bigger that the budget. Below we have the resulting figure.</p>

<center>
  {% include images/median_rentability_by_genre.html %}
</center>
  
<p align="justify">Until now, the analyses have covered the entire time period from 1959 to 2021. Now, it would be interesting to understand how genres evolve over time. A general decrease in rating score was perceived in a first analysis. Is it the case for all movie’s genre, and is this decrease significant? The movies are then divided into two periods, with 2000 as the cut-off point, when an increase in the number of movies is observed. The next figure reports the results on rating, revenue and budget, before and after the cut-off.</p>

  
<p align="center">
  <img src="images/old_recent_CIs.png" />
</p>
  
<p align="justify"> Romance, mystery, horror, history, documentary, comedy, biography, and animation movies were significantly better rated before 2000. Action movies and science-fiction show a (non-significant)  increase in rating score. All the other categories display a non-significant decrease of the average rating score.  The trend is similar for all genres, the ratings are decreasing.</p>
  
<p align="justify"> No movies show significant increase in their revenue, whereas romance, history, drama, crime, comedy, and biography movies have a significant decrease.</p>

<p align="justify"> Science fiction, adventure, and action movies show a significant increase in budget, whereas romance and drama movies undergo a significant decrease in their budget. </p>

<p align="justify"> Thus, a significant increase in budget (such as for action, adventure, and science fiction movies) does not reflect a significant increase in the revenue.</p>

<p align="justify"> In the second period, it seems harder to create movies as good as in the past. This could be due to the increasing concurrence. </p>
