# **NBA team Elo ratings may not be 100% accurate due to unforeseen circumstances.**

## **Part 1**
Sports have always been a hotbed of data that is scrutinized, analyzed and argued over. Throughout the years, one of the most heated arguments has been "who is the best". The best team. The best player. The best position. The best era. Like any NBA season, all pundits believe that there has to be a champion at the end of their argument season.

Now enter statistics. 

The NBA is littered with useful (WAR, EWA, RPM, %eFG) and useless (PER, PPG, FG%) acronyms for both players and teams. In an attempt to look at the impact of team ratings on the outcome of any typical game, I want to look at the Elo rating across the history of the NBA. Since the Elo rating creates a score for each team before  every game and adjusts after the game, it would be interesting to see the accuracy of this rating, or should we put it on the ever increasing pile of useless acronyms.

The Elo rating is a zero-sum calculation of the relative skill of a player or collection of players. It was created in the 1960's by Hungarian physicist, Arpad Elo, to more effectively rank chess players. Contemporary users of the Elo system include the NBA, MLB and even professional[Scrabble competitions](https://https://www.word-grabber.com/word-board-games/elo-ratings-in-scrabble). It is not an absolute measurement but a inferred measurement based on outcomes. The basic influencers of a team's Elo rating in the NBA are:

1. The final score of game. This not only includes which team won, but the margin of victory and game location.
2. A win relative to the probability of winning. For example, a team will gain more points for a victory over a team with a higher Elo. A team will lose more points for a loss to a team with a lower Elo.
3. All scores are calculated on a zero-sum basis. This means that if Team A gains 21 Elo points for a victory over Team B, then Team B will lose 21 Elo points.

If I had to make an assumption about what the results will be, I would lean towards a regression towards the mean over the history the league. I would also assume that the regular season results would skew higher or lower above the mean than for the entire history of the league.

## **Part 2**

#### List of resources that can be used for the project:
* fivethirthyeight - [How ELO is calculated](https://https://fivethirtyeight.com/features/how-we-calculate-nba-elo-ratings/)
  * This is an explanation of how Fivethirtheight has used Elo and calculated the scores. Also, it shows what features are used and the impact of those features on scoring. 

* fivethirthyeight - [History of NBA ELO](https://https://projects.fivethirtyeight.com/complete-history-of-the-nba/)
  *  Cool arcticle of how Elo is put into practice and what the Elo rating looks like for each individual team. Has a dropdown menu to look at each team.

* [Github Raw data](https://https://github.com/fivethirtyeight/data/tree/master/nba-elo)
  * Uhhh raw data. Also some explanation of what is going on.

* Wikipedia - [Elo Rating](https://en.wikipedia.org/wiki/Elo_rating_system)
  * Provides the standard wikipedia academic history and understanding of Elo rating. The math behind the calculations is included and can come in handy if I want to use other inputs and augment the way NBA uses Elo.
  
## **Part 3**

I was able to download the data and start to evaluate the dataset. I accessed the data with:

```
nba_data = pd.read_csv('https://raw.githubusercontent.com/fivethirtyeight/data/master/nba-elo/nbaallelo.csv')
```

My next steps should be:

1. To address the NaN elements of the data and figure what to do with them. Some data is not available for periods prior to the 1960's because those statistics were not measured prior to that time. This requires understanding the importance of specific metrics and relevance to other metrics.
2. Filter out what metrics I will omit from evaluation and sort determine how I will sort, group and divide the dataset.


## **Hemingway App Before and After of Part 1**

#### **Before**
![Image](https://github.com/hughjafro/DS-Sprint-03-Creating-Professional-Portfolios/blob/master/sprint-challenge/DS%2001%20Sprint%2003%20%20before.png)

#### **After**
![Image](https://github.com/hughjafro/DS-Sprint-03-Creating-Professional-Portfolios/blob/master/sprint-challenge/DS%2001%20Sprint%2003%20after.png)
