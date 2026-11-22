# How Psychological Framing Affects Economic Market Prices in the Lab and Field

- Authors / year: Ulrich Sonnemann, Colin F. Camerer, Craig R. Fox, and Thomas Langer (2013)
- Link / DOI: [PNAS article](https://doi.org/10.1073/pnas.1206326110) · [Full text](https://pmc.ncbi.nlm.nih.gov/articles/PMC3718178/)
- Version read and date:
- Why this paper is relevant: Tests whether individual judgment biases persist in prediction-market prices, connecting to Wolfers and Zitzewitz (2004) on information aggregation and market accuracy.

## Research question

Can a systematic bias in individual probability judgments shift prediction-market prices away from coherent probabilities, or will trading eliminate it?

## Main argument

The paper studies **partition dependence (PD)**: judgments about the probability of an event can change when the possible outcomes are grouped or split differently, even if the event itself is logically unchanged.

The authors find evidence of PD in market prices in four settings: a controlled laboratory market, a multiweek sports-market experiment, markets for macroeconomic indicators, and horse-race betting. Their conclusion is that markets do not always remove individual judgment biases; psychological framing can affect prices.

## Concepts and proposed mechanism

### Partitions, packing, and unpacking

A **partition** is a set of mutually exclusive categories that together cover the possible outcomes. A single event can be represented as one category (**packed**) or divided into explicit subcategories (**unpacked**).

For example, “Dow closes at or below 13,000” can be represented as one interval or as the union of “below 12,000” and “12,000–13,000.” These descriptions cover the same event. Normatively, the probability of the combined event should equal the sum of the probabilities of its parts:

`P(X ≤ 13,000) = P(X < 12,000) + P(12,000 ≤ X ≤ 13,000)`

Prior judgment research finds that people often assign a higher total probability when the interval is unpacked. Naming the subevents separately can make each one more salient and seem more likely.

### The “ignorance prior” at 1/N

The authors propose that, when people see `N` categories, they may start from a rough equal-probability anchor of `1/N` for each category and adjust insufficiently based on what they know. This is a proposed psychological mechanism, not an assumption that the outcomes are actually equally likely or that people consciously calculate `1/N`.

In the Dow example, “at or below 13,000” covers two of three categories in one partition, giving an equal-split anchor of `2/3`; in another partition, it covers one of three categories, giving an anchor of `1/3`. Residual anchoring can therefore make judgments differ even though the event is unchanged. The model helps predict when the bias may be larger: when the equal-split anchor is far from a well-informed probability.

### Why a market might preserve the bias

The “wisdom of crowds” can work when individual errors vary in different directions and average out. A systematic bias shared by many traders need not cancel. Market prices also weight opinions by trading activity, so well-informed, well-capitalized traders can sometimes outweigh biased traders. But whether trading reduces or magnifies a bias depends on incentives and trading conditions: informed traders may bet against a bias, or may find it profitable to trade with it. Capital constraints and short evaluation horizons can also limit aggressive arbitrage.

## Market and contract mechanics

The studies use contracts whose payoffs depend on whether a numerical outcome falls in a specified interval. A full set of interval contracts can approximate a probability distribution over the outcome. If one interval is split into two adjacent intervals, the two corresponding payoffs together should be equivalent to the payoff on the packed interval.

In the lab, participants traded using a continuous double auction: they could submit bids or asks, or trade against existing offers. In the field and historical datasets, market mechanisms included parimutuel betting.

## Data and methods

The authors combine four studies to compare controlled tests with naturally occurring markets:

1. **Short laboratory experiment:** 192 participants traded contracts on financial, sports, and weather outcomes. Groups saw alternative partitions, with selected intervals either packed or unpacked. Researchers also elicited individual probability judgments before and after trading.
2. **Multiweek sports-market experiment:** 456 participants traded over several weeks on NBA playoff wins and FIFA World Cup goals. The study compared prices and judgments for packed and unpacked intervals.
3. **Macroeconomic indicators:** The authors analyzed 153 parimutuel markets for four macroeconomic indicators. Digital-option contracts covered different intervals and were traded one to two days before data releases.
4. **Horse races:** The analysis used data on 6.3 million U.S. horse starts from 1992–2001, comparing market-implied probabilities with actual winning frequencies across races with different numbers of horses.

The experiments give researchers more control over how events are presented. The field data are more natural, but provide less control over why a particular partition was used. The authors argue that the methods complement one another.

## Main results

- **Lab:** Market prices showed substantial, persistent PD. Price differences between unpacked and corresponding packed intervals were 0.267 for financial outcomes, 0.229 for sports, and 0.149 for weather outcomes. Individual judgments also showed PD. Trading modestly reduced the effect, but did not eliminate it. Small price inconsistencies within a market were often arbitraged quickly; that did not remove the difference across partitions.
- **Multiweek sports markets:** The summed judgments for unpacked intervals exceeded judgments for comparable packed intervals by a median of 0.20 in NBA markets and 0.15 in World Cup markets. The effect was similar in scale to the lab and showed little visible convergence over time.
- **Macroeconomic markets:** Estimated prices were consistent with a positive weight on the equal-probability anchor for three of four indicators; there was no apparent effect for jobless claims. The estimated overall anchor weight was about 0.44 (`P < 0.01`). The authors still describe the markets as adequate forecasters, while noting that the probability distributions were distorted toward equal probabilities across traded intervals.
- **Horse races:** Long shots were more overbet relative to their actual winning probabilities in races with fewer horses, as the `1/N` account predicts. The estimated weight on the anchor was about 0.12, smaller than in the macroeconomic-market analysis.

The authors emphasize that the numerical anchor estimates differ across settings; they are not universal constants for prediction markets.

## Assumptions and limitations

- The `1/N` anchor is a proposed common explanation. It does not by itself prove the mental process of each trader.
- The controlled experiments help rule out alternative explanations, but may not capture every feature of naturally occurring markets. The field datasets are realistic, but less controlled.
- Individual studies may admit specialized alternative explanations. The authors’ case rests partly on the same PD pattern appearing across four distinct settings.
- The paper shows that framing can affect prices; it does not claim prediction markets are generally inaccurate. Markets may forecast well overall while still exhibiting systematic, localized distortions.
- Small price inconsistencies being arbitraged does not guarantee that every framing-driven price difference is corrected, especially when the relevant trades are across different market presentations or have limited liquidity.

## Concepts learned

- **Partition dependence:** probability judgments change with the grouping of possible outcomes.
- **Packing / unpacking:** presenting a union as one interval versus several named subintervals.
- **Ignorance prior:** the hypothesized equal split of probability across `N` presented categories, `1/N`.
- **Market aggregation:** prices reflect judgments weighted by trading activity, not a simple average of all participants.
- **Arbitrage versus framing:** arbitrage can fix some payoff inconsistencies without necessarily removing judgment biases embedded in demand.
- **Favorite–long-shot bias:** in horse racing, low-probability horses can be overbet; the paper tests the further prediction that the bias varies with the number of horses.

## Connection to this project

This paper suggests that contract **presentation and partitioning** may matter in addition to the underlying event and payoff. For related interval contracts, a useful check is whether a contract on a union of outcomes is priced consistently with the sum of contracts on its mutually exclusive parts.

For our project, that means relation discovery should capture payoff logic and outcome-set structure, not only semantic similarity. A candidate relation needs exact resolution criteria and compatible interval boundaries before it can be treated as an equivalence or arbitrage constraint. Execution still depends on fees, book depth, and whether the related positions can actually be traded.

The paper studies framing effects in judgments and market prices; it does not test NLP-based contract discovery.

## Questions to follow up

- Which alternative explanations does each study rule out, and which remain plausible?
- How should an arbitrage test distinguish a genuine payoff inconsistency from a framing-driven price difference across markets?
- Could contract interfaces reduce partition dependence by presenting equivalent interval decompositions together?
- How do liquidity, fees, and order-book depth affect whether a trader can exploit the price differences?
- What validation data would show whether a market’s implied probabilities are calibrated across different partitions?

## My short summary (from memory)
