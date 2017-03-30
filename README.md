<h1>Statistics</h1>

We made use of the standard error instead of the standard deviation. The standard deviation is a measure of the dispersion of the data from the mean. But we would like to measure how precise our estimate is of the mean. The main use of the standard error of the mean (SE) is to give confidence intervals around the estimated means for the mean and not for the data itself [L.15]. We want an confidence interval of 95\%, this means we can say there is only a 5\% chance that the range mean &plusmn; 1.96*SE excludes the mean of the population [AB05].

If we want to use the standard errors for confidence intervals, we have to make sure that the data is normally distributed. To make sure that we are dealing with a normal distribution. We can simulate a game e.g. 10,000 times and keep track of the expected scores. 

![Alt text](https://github.com/EloHackersz/SOM/blob/master/Statistics/histo_expected_score.png?raw=true "Expected score")

We also would like to use standard error for confidence intervals for the Elo rating of players. 

![Alt text](https://github.com/EloHackersz/SOM/blob/master/Statistics/histo_elo_rating.png?raw=true "Elo rating")

Both figures approximates a Bell curve  for these players. According to the Central Limit Theorem, the arithmetic mean of a sufficiently large number of iterates of independent random variables will be approximately normally distributed [ZR95]. Hence, we can say that the distribution of expected score of player 1 with skill 0.1 with player 2 with skill of 0.2 are normal. Therefore we may use the standard errors for confidence intervals and standard deviations. 

The confidence interval of 95\% can be calculated as:

![Alt text](https://github.com/EloHackersz/SOM/blob/master/Statistics/uplow.png?raw=true "Upper- and lowerbound")

The standard error of the mean can be calculated as:

![Alt text](https://github.com/EloHackersz/SOM/blob/master/Statistics/SE.png?raw=true "Standard Error")

The standard deviation can be calculated as:

![Alt text](https://github.com/EloHackersz/SOM/blob/master/Statistics/STD.png?raw=true#center "Standard Deviation")

<h1>Calculation of E<sub>A</sub></h1>

To gather the correct Elo ratings for all contestants, we are going to measure how precise our mean of Elo rating is. We will calculate the mean of the Elo rating over 10,000 matches. Because the Elo rating is normal distributed, see section 7 for more information, we will calculate a confidence interval of 95\% with the standard error of the mean.

The Elo rating is updated during each iteration of the simulation. First, the expected score per player is calculated using the already available Elo ratings. To keep the errors in the expected score, use Formula (1). To calculate the delta, we can calculate E<sub>A</sub> without the delta's of R<sub>A</sub> and R<sub>B</sub> Use the sum of the delta's &Delta;R of R<sub>A</sub> and R<sub>B</sub> to calculate the lower- or upper bound of the expected score, respectively Formula (2) and (3). To calculate the mean of the expected score use Formula (4). The error of the mean can be calculated with Formula (5). As the result of R<sub>A</sub>, see Formula (6).

(1) ![Alt text](https://github.com/EloHackersz/SOM/blob/master/EA/EA_normal.png?raw=true "Upper- and lowerbound")

(2) ![Alt text](https://github.com/EloHackersz/SOM/blob/master/EA/EA_lower.png?raw=true "Upper- and lowerbound")

(3) ![Alt text](https://github.com/EloHackersz/SOM/blob/master/EA/EA_upper.png?raw=true "Upper- and lowerbound")

(4) ![Alt text](https://github.com/EloHackersz/SOM/blob/master/EA/EA_mean.png?raw=true "Upper- and lowerbound")

(5) ![Alt text](https://github.com/EloHackersz/SOM/blob/master/EA/EA_error.png?raw=true "Upper- and lowerbound")

(6) ![Alt text](https://github.com/EloHackersz/SOM/blob/master/EA/EA.png?raw=true "Upper- and lowerbound")

<h1>References</h1>

[L.15] Hertzog L. Standard deviation vs Standard error. https://datascienceplus.com/standard-deviation-vs-standard-error/, 2015. Accessed 2017-03-28.

[AB05] D. G. Altman and J. M. Bland. Standard deviations and standard errors. Bmj, 331(7521):903, 2005.

[ZR95] E. R Ziegel and J. Rice. Mathematical statistics and data analysis, 1995.
