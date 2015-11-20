
#6:00 PM “They might be Robots, Using data for investment management and trading” Dan Von Kohorn, v2 Ratings
——————————————————————————————
#6:30 PM “Crowd-sourced Alpha: The Search for the Holy Grail of Investing” Jessica Stauth, Quantopian
###cluster analysis
* fun research project: minimally correlated strategies, perfect, perfect, per algo analysis
* thomas vickey, beysian statistics
* paper trading contest

###Active Trading
* your algorithm has to actively trade.  We measure that by looking at how often your portfolio turns over per year. 

###Low correlation to peers
* we look for algorithms with between -30% and +30% average pairwise correlation with the other algorithms in our portfolio

###strategic intent
* looking for algorithms that are driven by underlying economic reasoning
* Poor man’s “risk Premia and the VIX term Structure
* How do you expect it to work
* Need due diligence step of actually talking to people

###What we don’t look for
* overfitting, data snooping, spurious correlations
* Daily Returns Similarity = 85% consistency
* written in past and rewritten through version control 

###paper trading competition

###growth plan
* 5 or 10 strategies and then eventually find institutional strategies

#####www.quantopian.com/open
#####www.quantopian.com/fund
——————————————————————————————
#6:30 PM “How to Do Statistical Quantitative Finance from Your Bedroom” Delaney. Granizo-Mackenzie, Quantopian
* https://www.quantopian.com/lectures
* get familiar with ipynb
* ipython notebook you can split out the code in blocks and start seeing results in the notebook for academic research

###Linear Regresion
* Question: !!volatility
* 1.9271 better return on tesla relative to the S&P 500 (estimated over a very specific time period with specific constraints)
* Tesla is more volatile than S&P 500
* one of the first principles of quantitative finance
* The quality of math is directly proportional to your bank account (you are bad with you math, you could lose all your money tmrw)

###Beta Hedging (Beta Dependencies)
* Question: when you might make or lose money (!!Risk Exposure)
* made entire careers performing factor models and analysis
* shows tesla more volatile again
* looks like market explains movement in tesla
* ordering 93% of your money and putting it into the S&P
* how to reduce exposure to factors that you don’t trust
* one return stream, and other factor exposure return streams
* how to focus in on one dependency
* taking returns of tesla and short of market? A: reduced the mean returns short the market while market was performing well
* want consistent low exposure returns
* model proved that beta not consistent
* NEED TO HAVE PREDICTIVE CAPACITY (some instruments and methodologies perform better)
* alpha/beta tradeoff
* yahoo computes the same beta, up to you to see whether it is consistent

###Pairs Trading Strategy
* Question: no question, this is actually trading based on math
* Hypothesis: two models cointegrated, 
* compares two companies that manufacture the same product, or two companies in one supply chain.
* tangible economic link
* cointegration is when the difference between two time series follows a well defined normal distribution (similar but not the same as correlation)
* can’t say one p value is lower than the other, should only against 0.05 because anything more than that violates statistics
* want cointegration, not correlation
* take bet: if spread is large, going to take short on top and long on bottom
  * !!smaller in the future, bottom risen more than top, would make money (spread shrink make money, spread stays same (even)
  * !!could do vice versa: if spread is small, going to long top and short bottom (spread expands (make money), spread stays same (even)
* what about real securities that behave this way: look through set of securities (should be right 95% and wrong 5%) running a lot of test (use at your own risk)
  * rigorous approach: hypothesis: stocks that have economic linkage
  * alternative: get candidates, waiting and doing out of sampling 
* Multiple bias issue
* Add the market to variables of your analysis, could be related to market
* heat map of p values: ABGB & FSLR
* plot the spread
* constantly check for normality of things
* normalize spread to z score +/- 1
* long when below -1 and short when above +1, if cointegrated spread will make money
* (signal processing: subject to a tremendous amount of noise)
* use moving average to compute z score
* 60 days to build out that moving average

###!!Long-Short Equity
* past: where supposed to hedge out risk
* past: cool idea was to long and short in the market
* today: just a lot of leveraging
* survivability bias: how many people started that job, how many people left in response to the question of listen I have 3 years of positive tips
* Long Short: modular generic strategy: ability of your ranking scheme from differentiate high predictive returns to low predictive returns
  * create a basket of the bottom end (500 shares basket) equities short them, and top end (500 shares basket) go long on those
* if they are not moving with the market then market neutral
  * market is discrete
* overfit the data will be a mistake in your data science
* math says you are making money on the spread from low to high while keeping market neutrality
* choosing a ranking scheme is very complicated, full notebook on lecture series on evaluating ranking scheme
  * spearman-rank correlation
  * modular strategy
  * could be mean reversion
* accept the fact that you are inaccurate, but may be able to observe trends
* !!Long-Short Equity model goal: on average you will get some nice consistent returns

###how do you trade to make money on that, and then test it on this

###Questions
* check for correlation between your sectors
* compare between ETFs
* Risk Factor Exposure: computed beta: always check for normality
* Returns on S&P is not a normal system
* Pairs Trading Strategy: if long enough time frame then it would have cointegration, but need a reasonable time frame to make trades, could find some stocks that work well on it, another strategy idea could do Pairs Trading on sectors

* What is Fama french factors
* also get fundamentals
* getting factor modeling API so the mechanics are there in the near future

* can import your own data in the factor environment

###!!Quandl.com (provides all sort of data points)
* can export .csv link and pull into Quantopian
* can’t call handwritten code
* have script on your own machine that feeds into .csv and then put into Quantopian that way
