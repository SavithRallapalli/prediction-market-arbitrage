# Prediction Market Combinatorial Arbitrage

Research project on discovering logical relationships between prediction-market contracts and testing whether apparent price inconsistencies are executable after spreads, depth, and fees.

The project is inspired by Shi and Zhai, [“Combinatorial Arbitrage in Prediction Markets”](https://arxiv.org/abs/2610.23517), and Saguillo et al., [“Unravelling the Probabilistic Forest”](https://arxiv.org/abs/2508.03474). The planned machine-learning component retrieves and classifies candidate contract relationships. Explicit payoff constraints and execution-cost calculations determine whether a candidate is a valid arbitrage under the modeled assumptions.

## Research question

Can machine-learning-assisted relation discovery identify useful logical relationships between contracts while keeping false arbitrage claims low?

## Planned pipeline

1. Collect market metadata, resolution rules, and public order-book snapshots.
2. Retrieve candidate contract pairs using structured metadata and text embeddings.
3. Classify candidate relations with a fine-tuned natural-language-inference cross-encoder, including an abstain/unclear option.
4. Convert reviewed relations into possible joint payoff states.
5. Check price coherence and simulate execution against displayed depth, fees, and conservative size limits.

## Planned technology

- Python for collection, modeling, and analysis.
- DuckDB and Parquet for local research data.
- Sentence Transformers for candidate retrieval, followed by a fine-tuned NLI cross-encoder (initial baseline: `cross-encoder/nli-deberta-v3-base`) for relation classification.
- OR-Tools for constrained portfolio optimization once the payoff model is validated.
- Jupyter for research; a small Streamlit dashboard is optional.

The NLI model is a starting baseline, not a prediction-market-specific model. Relations will be evaluated on manually reviewed labels, with event-grouped splits and an explicit abstain/unclear outcome.

The model proposes relationships; payoff logic verifies them. This is a research and paper-trading project. It does not require live orders or real-money trading.

## Repository layout

```text
notes/          Reading notes, concept ledger, and project log
data/           Data documentation; raw data is not committed
notebooks/      Exploratory research notebooks
src/            Reusable project code
tests/          Focused checks for payoff and execution logic
```

## Getting started

Requires Python 3.11 or newer.

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
python -m pip install -e '.[dev]'
```

The initial scaffold intentionally contains no live trading credentials or order-placement code. Start with a small, manually reviewed set of contracts and recorded public data.

## Research safeguards

- Split training and evaluation data by event or event family to reduce leakage.
- Report relationship precision and false-positive rates, especially for implication and exclusivity.
- Keep ambiguous contract pairs out of guaranteed-payoff claims.
- Distinguish quoted-price gaps from executable opportunities.
- Document API coverage, missing historical book data, fees, and other assumptions.

## Status

Research setup and reading phase. Implementation scope will be finalized after the literature review and data audit.
