# Improvement to an Existing Strategy
--- Part 5 ---

---
This part will discuss an improvement to the trading strategy development in the previous part (part 4). I am actually using this improvement in my real trading account.

## Disclaimer !!!

**I do not recommend that anybody follow my strategy, as I cannot guarantee this strategy will continue to deliver positive results in the future**. **Alpha-decay** (a decay of an algorithmic trading performance) is a real phenomenon, and you should know about it.

I ran the strategy across several forex pairs and indices, and each market has its own setting tailored to its market characteristics. You cannot only rely on one pair/market and hope it will constantly print money. Each market has its own period of several consecutive losses, even though in the long run it still delivers positive results. By deploying the strategy on several markets, any consecutive loss period would be covered by profits from other markets.

One more thing, all of the strategy codes presented in this article are the simplified versions of what I am using right now. The simplifications are made to ease the understanding of the underlying logic behind the strategy. You cannot just use the code presented here to trade on a real account. These codes are enough to conduct a backtest and optimization, but still need many additional codes to be run on a real account.

---

## Background
During the development process of the previous trading strategy on the USDJPY pair for the Daily timeframe, I noticed something interesting. There are many cases of the sell stop order is triggered, the price falls straight to the take profit level, and then bounces up to the entry level or beyond. This got me thinking, "hmmmm... What if I put a buy limit order somewhere near the take profit level?". Interesting right?
