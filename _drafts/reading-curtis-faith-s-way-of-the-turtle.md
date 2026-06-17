---
layout: post
title: Reading Curtis Faith's "Way of the Turtle"
category: Notes
tags: [economy, finance, trading]
media_subpath: /assets/img/posts/reading-curtis-faith-s-way-of-the-turtle
image: cover.jpg
math: true
---
*Way of the Turtle* (2007) is a memoir, trading manual, and philosophy of systematic investing written by Curtis Faith, the youngest and most successful member of the legendary Turtle Traders. The book recounts the famous experiment by Richard Dennis and William Eckhardt to determine whether great traders are born or made. They recruited ordinary people, trained them for just two weeks, and entrusted them with millions of dollars to trade.

## Foreword by Van K. Tharp

> In my opinion, *this is one of the five best trading books ever written*, and I will recommend that all my clients become familiar with its contents.

What are other four best books?

> In my opinion, their success was due entirely to their psychology and their position sizing.

The Turtles didn't have magic.

## 1. Risk Junkies

The difference between investors and traders:

> Investors are people who buy things for the long haul with the idea that over a considerable period—many years—their investments will appreciate in value.

Traders do not buy actual things; they buy or sell risk.

> In his informative and engaging book *Against the Gods: The Remarkable Story of Risk*, Peter Bernstein discusses how markets developed to allow the transfer of risk from one party to another. This is indeed the reason financial markets were created and a function they continue to serve.

### Traders Trade Risk

There are two types of risk: liquidity risk and price risk.

Liquidity risk refers to that a trader will not be able to buy or sell.

You always face two prices in the quote: the bid and ask prices. Usually, the ask price is higher than the bid price; the difference between them is called *spread*. If you want to buy an asset, you have to buy it at the ask price; if you want to sell it, you have to sell it at the bid price. Thus, every moment you buy or sell an asset, you get a cost due to the spread. The larger the spread, the lower the liquidity of the asset because the larger trading cost would make you hesitate to trade.

Traders who trade liquidity risk are called *scalpers* or *market makers*. They make money off the spread.

Price risk refers to the possibility that prices will move significantly up or down.

Traders who jump on price risk are known as *speculators* or *position traders*.

## 2. Taming the Turtle Mind

> The field of behavioral finance—brought to popular attention in Robert Shiller’s fascinating book, now in its Second Edition, titled *Irrational Exuberance* and greater details of which were published by Hersh Shefrin in his classic *Beyond Greed and Fear*—helps traders and investors understand the reasons why markets operate the way they do.

### Emotional Rescue

> The Turtle Way works and continues to work because it is based on the *market movements that result from the systematic and repeated irrationality that is embedded in every person.*

Here the author mentions some cognitive biases:

- **Loss aversion**  
  People prefer to avoid losses rather than to acquire gains. Loss aversion affects one’s ability to follow mechanical trading systems because the losses incurred in following a system are felt more strongly than are the potential winnings from using that system.
- **Sunk costs effect**  
  Sunk costs are costs that already have been incurred and cannot be recovered. People considering sunk costs would hesitate to stop loss.
- **Disposition effect**  
  The disposition effect is the tendency for investors to sell shares whose price is increasing and keep shares that have dropped in value. This tendency would make winning trades unable to cover losses.
- **Outcome bias**  
  Outcome bias is the propensity to judge a decision by its outcome rather than by the quality of the decision at the time it was made. Even a "correct" trade would make a loss; if you have outcome bias, you would doubt your trading system.
- **Recency bias**  
  Recency bias is the tendency for individuals to place greater importance on more recent data and experience.

### The Turtle Way

There are many trading styles, and the author doesn't believe that there is a best style.

#### Trend Following

> In trend following, the trader attempts to capitalize on large price movements over the course of several months.

This is not a strategy easy to follow because

1. Large trends happen infrequently, and it means that this strategy generates a much higher percentage of losing trades than winning trades.
2. It loses when the trend reverse.
3. It requires a relatively large amount of money to trade using reasonable risk limits because of the large distance between the entry price and the stop loss price.

#### Countertrend Trading

> A countertrend trading style makes money when markets are not trending by using a strategy that is the opposite of trend following.

#### Swing Trading

> Swing trading is essentially the same as trend following except that it targets shorter-term market moves.

#### Day Trading

> A true day trader looks to exit the market before it closes each day. ... Day traders generally use one of three different trading styles: position trading, scalping, or arbitrage.

### Watching the Market State

> A Turtle never tries to predict market direction but instead *looks for indications that a market is in a particular state.*

## 3. The First $2 Million Is the Toughest

> *Trade with an edge, manage risk, be consistent, and keep it simple. The entire Turtle training, and indeed the basis for all successful trading, can be summed up in these four core principles.*
{: .prompt-tip }

### Risk of Ruin

> In gambling, risk of ruin refers to the possibility that you will drop all your money because of a string of losses.

We need to design an algorithm for calculating the size of each trade so that we won't be swept out even after a string of losses.

### The Science of Controlled Risk

The Turtles use the *average true range* to determine the trade size:

> That is the name given to it by J. Welles Wilder in his book *New Concepts in Technical Trading Systems*.

> The concept of adjusting trade size on the basis of volatility (position size) has been written about by others, most notably by Van Tharp in his 1998 book *Trade Your Way to Financial Freedom* and the second edition of that book, published in 2007.

### The Turtle Edge

> The Turtles were taught to use limit orders rather than market orders, which we did most of the time. Large market orders invariably move the price.

For example, if you decide to enter a market, you could place a limit order at the lowest price of the last 10 minutes.

> Trading methods that work over the long run have what is known in gambling as an *edge*. An edge refers to one’s systematic advantage over an opponent.

### Trend Following

> The specific method we used was known as the breakout, sometimes referred to as Donchian channels after Richard Donchian, who popularized the breakout method of trading. The basic idea was to buy if a market exceeded the highest price for a particular number of preceding days, that is, *broke out* of its prior price levels. We had an intermediate-length system that Rich and Bill called *System 1* that considered 20 days (or 4 trading weeks) of prices to determine the highs and lows and a longer-term system, *System 2*, that used 60-day (12-week) highs and lows to determine the breakout. We would calculate the most extreme highs and lows for each system at the end of each day. Generally, this meant looking back to determine one or two prices that were the high on the basis of their visual appearance. Most days, the highs would remain the same and there would be no work to do. Each system had two types of exits. The first was a stop loss exit that was a maximum of $2N$, or two average true ranges away from the entry point. This also happened to represent 2 percent of our account because the way we determined the number of contracts to trade per market also was based on $N$ (average true range).

## 5. Trading with an Edge
