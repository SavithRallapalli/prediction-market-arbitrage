# Prediction Markets

- **Authors:** Justin Wolfers and Eric Zitzewitz
- **Published:** 2004, *Journal of Economic Perspectives*, 18(2), 107–126
- **DOI:** [10.1257/0895330041371321](https://doi.org/10.1257/0895330041371321)
- **Full text:** [AEA PDF](https://pubs.aeaweb.org/doi/pdfplus/10.1257/0895330041371321)
- **Version read / date:**
- **Reading status:** Guide prepared; reading not yet started

## Why this is first

This is the broad foundation for the project: what prediction-market contracts pay, how prices can be interpreted as forecasts, and why market design and limitations matter. The paper also discusses arbitrage and manipulation, and notes that complex contingent and combinatorial markets were still largely untested at the time.

## Reading route

Read the full 20-page article once. On the first pass, focus on the argument and examples rather than trying to follow every cited study.

| Part | Pages | Questions to carry into the reading |
|---|---:|---|
| Introduction | 107–108 | What do the authors mean by a prediction market? What does the Poindexter example illustrate about prices and news? |
| Types of Prediction Markets | 109–111 | How do winner-take-all, index, and spread contracts differ in the quantity their prices reveal? What assumptions are needed to read price as probability? |
| Applications and forecast accuracy | 111–118 | What kinds of evidence do the authors use for forecast quality? What comparisons or caveats matter? |
| Market design | 119–121 | How do the trading mechanism, contract wording, incentives, and available information affect whether a market works? |
| Making inferences from markets | 122–124 | What can prices reveal about beliefs or relationships between events? Why is correlation not automatically causation? |
| Future applications and conclusion | 124–125 | What do the authors say about contingent and combinatorial markets? What do they identify as the markets’ useful roles and limits? |

## Research question

How well can markets with contracts tied to future events aggregate dispersed information into useful forecasts, and what contract designs and market conditions support that role?

## Preview from the abstract

The authors survey evidence from several prediction-market settings. They argue that market-generated forecasts are often fairly accurate and competitive with moderately sophisticated benchmarks. They also explain that contract design can make prices informative about different quantities—not only event probabilities—and discuss design issues and limitations.

Treat this as a preview to check against the paper, not as a substitute for your own summary.

## Notes from my reading

Prediction/Information Markets (Event Futures): Markets where participants trade in contracts whose payoff depends on unknown future events.

According to the efficient markets hypothesis, in a truly efficient prediction market, the market price will be the best predictor of the event, and no combination of available polls or other information can be used to improve the market generated forecasts.

All traders need not be rational for this to work out, only the marginal traders (the traders who are currently trading on the current price) matter. This is because rational traders orders almost all of the time counterbalance the less informed trades and move the price towards what their information implies. 

The paper isn't discussing markets like sports betting where the focus is holding or trading risk that may be intrinsically enjoyable. It also isn't discussing markets that are large enough to allow risk management and risk sharing, like major financial markets. The main focus is on information transmission, though this 3 divisions aren't impermeable. 

Types of Contracts:

1:"winner-take-all" contract:

The contract costs some amount $p, and pays of $1 if and only if a specific event occurs. 

The price of a winner-take-all market represents the market's expectation of the probability that an event will occur (assuming risk-neutrality) 

What does assuming risk neutrality mean: A risk neutral trader cares about the contracts average dollar payoff (weighed by how likely each outcome is). They don't need extra compensation for bearing the risk. 

Suppose a contract costs #p, pays $1 if the event happens, pays $0 otherwise. If the trader thinks the event has a probability q, the expected payoff is q*$1. A risk neutral trader is willing to buy at any price below q, but unwilling to buy above q. 

Being risk averse changes the payoff, and make the value of a risky payoff less than its average dollar amount, because they dislike uncertainty. They might pay less than q for the same contract. That gap is a risk premium, and the price alone no longer reveals their probability. 

If an event is tied to a trader's own financial wellbeing, the contract may pay precisely when the trader needs the money the most, which can push the price away from the probability. 

2:"index" contract:

The amount that the contract pays varies in a continuous way based on a number that rises or falls. The price for such a contract represents the mean value that the market assigns to the outcome. 

The payoff is ultimately the same in the two types of contracts. They represent different interpretations though: for a yes/no payoff the expected payoff is a probability, for a varying numerical payoff, it is the mean forecast of that number. 

3:"spread" betting: 

The traders differentiate themselves by bidding on the cutoff that determines whether an event occurs, like whether a candidate receives more than a certain %age of the popular vote. 

When spread betting is combined with an even money bet (double or nothing), the outcome yields the market's expectation of the median outcome, because that's the fairest best (if payoff is as likely to occur as not).

LLM Explanation: 
"Let’s use one event throughout:

> **Event:** What share of the popular vote will Candidate A receive?

Suppose traders have looked at polls, turnout, and other information. For illustration, imagine their combined forecast looks like this:

| Candidate A’s vote share | Forecast probability |
|---:|---:|
| 46% | 20% |
| 50% | 30% |
| 54% | 30% |
| 58% | 20% |

This is a simplified forecast distribution, not a claim that real forecasts have only four possible outcomes.

### 1. Winner-take-all contract: “Will A get more than 50%?”

The contract pays **$1 if A gets more than 50%**, and $0 otherwise.

A gets more than 50% in the 54% and 58% outcomes, whose probabilities add up to \(30\%+20\%=50\%\). So the expected payoff is:

\[
\$1 \times 0.50 + \$0 \times 0.50 = \$0.50
\]

Under the risk-neutral assumption, the contract price would be about **50¢**. This price represents the forecast probability that A gets more than 50%.

### 2. Index contract: “What vote share will A get?”

Now imagine a contract that pays **$1 for each percentage point** of A’s vote share. If A gets 54%, for example, it pays $54.

The mean forecast is:

\[
(46 \times .20)+(50 \times .30)+(54 \times .30)+(58 \times .20)=52
\]

So the contract’s expected payoff is **$52**, and its price would be about $52 under risk neutrality. This represents the market’s **mean vote-share forecast: 52%**.

The index price averages the *size* of the possible outcomes, weighted by their probabilities.

### 3. Spread bet: “Will A get more or less than 52%?”

Suppose the bet pays even money: win $10 if you’re right, lose $10 if you’re wrong. Traders choose the cutoff.

At a cutoff of **52%**, the “over” side wins when the result is 54% or 58%: probability \(30\%+20\%=50\%\). The “under” side wins at 46% or 50%: also 50%. So neither side has an advantage at even money. The fair cutoff is **52%**, the median of this forecast distribution.

The spread reveals the point that divides the forecast outcomes in half. In this example, the mean and median both happen to be 52%; they need not be equal in other forecasts.

So, from the same underlying forecast:

- **Winner-take-all price:** 50¢ → 50% chance A exceeds 50%.
- **Index price:** $52 → mean forecast of 52% of the vote.
- **Even-money spread:** 52% cutoff → median forecast of 52% of the vote."





<img width="475" height="227" alt="Screenshot 2026-11-22 at 00 28 50" src="https://github.com/user-attachments/assets/a45a1753-d669-4e51-9ae1-7cb4132a635c" />

The basic forms of these contracts reveal market expectations for a specific parameter: a probability, mean or median. But in addition, prediction markets can also be used to evaluate uncertainty about these expectations. For instance, a family of winner-take-all contracts that pay off if and only if the candidate earns a 48%, 49%, 50% and so on. This family of winner-take-all contracts will then reveal almost the entire probability distribution of the market's expectations. A family of spread betting contracts 

An even-money bet in a spread contract will
define the median, as explained above. But for similar reasons, a contract that costs $4 and pays $5 if y  y* will elicit a value of y* that the market believes to be a four-fifths probability, thus identifying the 80th percentile of the distribution.

Non linear index contracts can reveal even more information:
For instance, consider a market with two index contracts, one that pays in a standard linear form and another that pays according to
the square of the index, y2
. Market prices will reveal the market’s expectation of
E[ y2
] and E[ y], which can be used to make an inference about the market’s beliefs
regarding the standard deviation of E[ y], more commonly known as the standard
error. (Recall that the standard deviation can be expressed as E y
2
  Ey
2
, or
the square root of the mean of the squares less the square of the means.) By the
same logic, adding even more complicated index contracts can yield insight into
higher-order moments of the distribution.

Accuracy of Prediction Markets:

Empirically shown to beat alternatives like polling. Prediction markets are also known to work well at higher levels of granularity, which might not be profitable for alternative providers because of the funding required. 

The strongest numerical comparison comes from election results. But this does not establish that the market always beats other forecasting methods.

Possibilities for Arbitrage:

There are several ways of looking for arbitrage opportunities: whether prices for similar contracts can be arbitraged across different exchanges or different securities or whether predictable patterns in the movement of the prices allow for arbitrage; and whether arbitrageurs might be able to exploit predictable deviations from rationality. 

Prediction markets do seem to display some of the deviations from perfect rationality that appear in other financial markets. There is substantial evidence from psychology and economics suggesting that people tend to overvalue small probabilities and undervalue near certainties. 

This may mean that prediction markets may perform poorly at predicting low probability events.

The passage is warning that **market prices can be systematically biased at the extremes**. Since traders often interpret a yes/no contract’s price as a probability, that bias can make low-probability events look more likely than they really are.

### The horse-racing example

A *long shot* is a horse with a small chance of winning; a *favorite* has a high chance. The **favorite–long-shot bias** is the tendency for bettors to put too much money on long shots, making their odds worse than the horse’s true chance justifies.

For a simple illustration, suppose an event truly has a **1% chance**. A perfectly calibrated $1 contract paying $100 if it happens would have a fair price of $1. But if traders treat the event as having a 3% chance, they might pay around $3 for that payout. Anyone buying at that price loses money on average: a 1% chance of receiving $100 is worth $1 in expected payout, not $3.

The same bias can make favorites look slightly less likely than they really are. Bettors who choose favorites may therefore get somewhat better odds—but, as the authors emphasize, their average returns are still negative.

### The options-market comparison

An **out-of-the-money option** pays only if the underlying asset makes a sufficiently large move. That payoff is relatively unlikely. The passage says such options have sometimes been priced higher than standard option models would predict. Conversely, **deeply in-the-money options**, whose payoff is much more likely, have sometimes been priced lower than those models would predict.

The analogy is that markets may place extra value on a small chance of a big payoff, while discounting outcomes that are already very likely. The paper is describing an observed pricing pattern, not saying every option market or every contract follows it.

### Why this matters for prediction markets

Suppose an event really has a 1% chance, but its market price implies 3%. If you treat the price as the probability, you’ll overestimate the event’s likelihood. Prices near 0% or 100% may therefore be less well calibrated than prices in the middle.

**The paper’s claim is cautious:** these patterns in other markets suggest that prediction markets *may* perform poorly on small-probability events. It is a reason to check calibration—whether events priced around 1% actually happen about 1% of the time—not proof that every low-probability prediction-market price is wrong. ([Wolfers & Zitzewitz, “Prediction Markets,” pp. 117–18](https://pubs.aeaweb.org/doi/pdfplus/10.1257/0895330041371321))


Another behavioural bias reflects the tendency of market participants to trade according to their predispositions. Ex. Traders buy and sell in political markets in a manner correlated with their party identification.
Even so, as long as marginal trades are motivated by profits rather than partisanship, prices will reflect the assessments of (unbiased) profit motive. Thus far, there is little evidence that these factors yield systematic unexploited
profits.

In their seminal paper, "The Limits of Arbitrage" (Journal of Finance, 1997), Shleifer and Vishny challenge the traditional Efficient Market Hypothesis (EMH) assumption that rational arbitrageurs will immediately correct any price distortion caused by irrational "noise traders."

Core Mechanisms Behind Bubble Persistence

• Noise Trader Risk (Widening Mispricing): Even if an asset is clearly overpriced, irrational sentiment can push the price even higher in the short term before it eventually reverts to its fundamental value.
• Capital Constraints and Redemptions: Professional arbitrageurs manage other people's money. When a bet temporarily moves against them because a bubble inflates further, investors in their funds see short-term losses and withdraw their capital—forcing the arbitrageur to liquidate their position at a loss right when the arbitrage opportunity is actually most attractive.
• Short-Selling Constraints: Shorting an overpriced asset carries asymmetric risk (unlimited potential loss vs. capped gain) and practical hurdles, such as high borrowing fees, difficulty locating shares to borrow, and the risk of a forced buy-in (short squeeze).
• Risk Aversion and Concentration Limits: Because of the risk that mispricing deepens in the short run, rational investors are unwilling to commit a massive portion of their wealth to a single arbitrage trade, leaving insufficient capital to push prices back to fundamental levels.

Real-World Example: The Dot-Com Bubble

During the late 1990s, several prominent hedge funds (such as Julian Robertson’s Tiger Management) recognized that technology stocks were severely overvalued and shorted them. However, tech valuations continued to soar for months. Facing heavy paper losses and massive investor redemptions, these funds were forced to close their short positions near the peak—just months before the bubble finally burst in 2000.

Can Event Markets Be Easily Manipulated:

The profit motive has usually proven sufficient to ensure that manipulation attempts were unsuccessful. The extent to which markets are manipulable depends on how thin they are.

Market Design:

The authors’ main point is that prediction markets need more than a clever pricing mechanism. They also need clear contracts, active traders, useful information, and a way to bring traders’ views together.
- How trades happen: Markets can match buyers and sellers through bids and asks, pool bets and divide the pot among winners, or use a market maker who posts prices. More complex systems can combine predictions across many possible outcomes.
- Clear resolution rules: A contract must specify exactly what counts as “yes” and when the answer will be determined. Ambiguity can cause trouble even when the contract initially seems clear: vote counts can change, politicians can switch parties, and project deadlines can be revised.
- Real money versus play money: Real money may motivate research, but play-money markets can also forecast well. In one football-season comparison, the two types performed about equally and both beat most participants in a large online contest. The authors say the evidence was too limited to conclude that one type was generally more accurate.
- Reasons to trade: People need an incentive to participate. Entertainment, competition, or prizes may be enough for small markets. Trading also needs disagreement: if everyone shares the same information and beliefs, there may be little reason to trade.
- Information and participation: Widely discussed events may work well because they attract traders and provide public information to interpret. A market dominated by a few people with much better private information can discourage everyone else from trading, leaving the market thin.
- Limits of aggregation: Markets can reward people for finding information, sharing it through trades, and combining different opinions. But they cannot reliably produce good forecasts if the available information is poor, misleading, or incomplete. In that situation, prices may simply aggregate the same bad information as everyone else.

Making Inferences:

The authors describe using prediction-market prices in three ways:
- As forecasts: For example, a company can use a market’s sales forecast directly in its planning.
- Alongside other data: Researchers can compare market prices with oil prices, stock prices, or other measures. But seeing two things move together does not establish that one caused the other; reverse causality and omitted factors may explain the relationship.
- Through conditional contracts: A contract can reveal what the market expects if a particular event happens. Comparing oil-price contracts conditional on Saddam being ousted or remaining in power could show the market’s expected oil price in each scenario.
The 2004 Iowa election market provides an example of conditional contracts. Contracts on a Democrat’s and a Republican’s vote shares paid only if that Democrat won the nomination. Because the two vote shares add to 100%, combining the contracts revealed the candidate’s implied probability of winning the nomination. Dividing the Democratic vote-share contract price by that probability gave the expected Democratic vote share conditional on that candidate being nominated.

In the table, Kerry was most likely to win the nomination, but Edwards had the highest expected vote share if nominated. The authors suggest delegates could consider that when choosing a nominee.

Their caution: Conditional forecasts don’t automatically identify causal effects or a candidate’s underlying ability. For example, Edwards might be expected to win only in scenarios where Democrats are already energized. Those same scenarios could also make Democrats more likely to win the general election. More contracts might measure some factors behind nomination outcomes, but some important factors are hard to observe or contract on.

In short: Conditional markets can provide useful forecasts for different scenarios. But using them to decide what would cause a better outcome requires care, and the authors note that these markets had barely been tested.






### Main argument, in my own words


### Market and contract mechanics I learned


### Evidence and examples that persuaded me


### Assumptions behind reading price as probability


### Limitations or counterarguments


### Concepts to add to `../concepts.md`


### Connection to combinatorial arbitrage

- Which contract types in this paper have related or contingent payoffs?
- What would it mean for related prices to be logically coherent?
- Which mechanisms could create, preserve, or remove a price inconsistency?

### Questions to follow up

-

### My short summary (write from memory after reading)


## After-reading check

- Can I explain why a binary contract price may be interpreted as a probability, and state the assumptions behind that interpretation?
- Can I distinguish a market forecast from the average belief of individual traders?
- Can I explain the difference between a price discrepancy and an executable arbitrage?
- What important parts of today’s prediction-market structure are outside the scope of this 2004 review?
