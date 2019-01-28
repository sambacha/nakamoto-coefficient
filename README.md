# ![nakamoto logo](assets/logo.png ) Nakamoto Coefficient

A Python library for measuring the Nakamoto Coefficient of a Sector.
Based on the post ["Quantifying Dectralization"](https://news.earn.com/quantifying-decentralization-e39db233c28e?gi=26ec1a01794a)

![nakamoto plot](assets/plot.png)

Features:
- Nakamoto Coefficient Measurement
- [Gini](https://www.investopedia.com/terms/g/gini-index.asp) Coefficient Measurement
- Lorenz Curve Plot on [Plotly](https://plot.ly/)
- Decentralization Plot (Lorenz + Nakamoto Features)
- Custom + Built In Sectors (See Sectors section)

## Installation Instructions

```
$ pip install nakamoto
```

## Running Tests

Make sure to sign up for Plotly to get an API Key, as well as get a Github API Key.
Github and Market URL Environment Variables aren't required to run full test script below.

```
PLOTLY_USERNAME=X PLOTLY_API_KEY=Y GITHUB_URL=Z GITHUB_API=A MARKET_URL=B python3 test.py
```

## Sectors

### Custom Sectors
This module allows passing a numpy array of data to be processed in order to measure inequality distribution (gini) and decentralization
(nakamoto coefficient). We use `CustomSector` for that. Check out the examples.

### Repository
Measures Github contributions of all who contribute to a specific repository and determines
how decentralized the repository is and the minimum number of developers needed to compromise it.

### Market
Measures volume by cryptocurrency exchange using data from CoinMarketCap for a specific currency.
Measures how centralized exchanges are in respect to a particular volume of a cryptocurrency and 
minimum exchanges needed to centralize volume.

### Client 
Measures decentralization by client usage. Currently scrapes data for combined EVM nodes. Future versions aim to separate the data 
and have more coins.

### Geography
Measures miner decentralization by country. Sames as `Client`, measures for combined EVM nodes. Future versions aim to separate 
the data and have more coins.
