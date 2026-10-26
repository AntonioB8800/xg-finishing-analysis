# Is finishing a repeatable skill?

An expected goals (xG) model built on StatsBomb open data.

> Work in progress — updated weekly until December 2026.

## The question
Some strikers are labelled "clinical finishers" and others are said to "not deliver".
But a striker can underperform for two very different reasons: missing good chances,
or not getting good chances in the first place.

This project builds an xG model to separate the two, and then tests whether
scoring more than your xG is a **repeatable skill** or mostly **noise**.
That matters for any club paying a transfer premium for "finishing".

## Data
[StatsBomb Open Data](https://github.com/statsbomb/open-data), loaded with `statsbombpy`.

**Coverage check:** before modelling, I checked how many matches each
competition-season contains. Many seasons are incomplete; for example,
La Liga 2018/19 contains only Barcelona's 34 matches, not all 380.
Using every shot would over-represent one team, so the model uses
**only complete competition-seasons**.

## Approach (planned)
1. Build a clean dataset of shots from complete competition-seasons
2. Engineer features: distance and angle to goal, body part, shot type, pressure
3. Train and evaluate xG models (logistic regression, gradient boosting)
4. Compare goals vs xG per player and test whether over-performance persists

## Progress
- [x] Project setup and environment
- [x] Data exploration and coverage check
- [ ] Shot dataset
- [ ] Feature engineering
- [ ] xG model
- [ ] Finishing skill analysis
- [ ] Final write-up

## How to run
```
git clone https://github.com/AntonioB8800/xg-finishing-analysis.git
cd xg-finishing-analysis
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```
On Mac/Linux, activate with `source .venv/bin/activate` instead.

## Author
António Barnabé, BBA & BBAI student at ESADE
