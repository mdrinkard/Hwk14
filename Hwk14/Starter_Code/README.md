# Machine Learning Trading Bot

In this Challenge, you’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. Your firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, your firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave your firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. You’re thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, you’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

# Evaluation Report

1) BaseLine

The Baseline algorithm uses the sma of two indicators the long and short indicator. These create signals that indicates a sell or buy signal if the line crosses that indicator. 

After running this strategy against the actual market close price changes we see the indicator initially outperforms that actual returns generated from the difference in closing prices. This green period lasts until early 2016 where the the actual returns start to outpace the strategy returns by a significant margin. 

As the actual returns are based only on the change in closing price, this seems to indicate that while stock prices are growing the algo performs sub-optimally as the volatility spikes are making the algo sell early or short at a bad time.

2) Tuning

The original parameters for the model are a 3month date offset for the data I selected to test, a 100 day long window, and a 4 day short window. In the 6month version I doubled all of these parameters and in the 1m version I set the date offself to 1 month and divided all other parameters by 2. I also ran the algo through the ADAdaybooster model and the logistical regression model. 

I found that the larger the I made the parameters the more my strategy returns failed to perform against the actual returns. 

3) Analysis

It appears that the models I ran do not improve the models accruacy much. What made the most impactful change was changing the short and long windows to the algorithm. This seems to suggest that the model suffers from a signal line that is too sensitive to volatility changes as it is getting crossed despite the general uptrend on the stock price.
