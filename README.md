# Crypto Screen · TradingView

This branch maintains the compact TradingView version. The original Binance API monitor is maintained on [`main`](https://github.com/Maruegg258/Crypto-screen/tree/main).

## TradingView tab view

Open [`tradingview.html`](tradingview.html) for the compact TradingView version:

- BTC, ETH, and HYPE tabs above a single Symbol Overview widget
- Binance USDT perpetual contracts (`BINANCE:BTCUSDT.P`, `BINANCE:ETHUSDT.P`, `BINANCE:HYPEUSDT.P`)
- Dark theme, native price and percentage change, an area chart, right-hand price scale, and pointer inspection
- Native 1D / 1W / 1M range buttons; no explicit initial range is supplied by the wrapper
- TradingView controls time/price axes, time-label formatting, and automatic market-data updates
- TradingView attribution and a direct link to the selected contract
- Keyboard tab navigation and a retry button if the embed cannot load
- One selected widget at a time; switching symbols removes the previous embed

This is a standalone HTML file with no build step, framework, API key, or backend. TradingView supplies the embedded market data and controls its update frequency, availability, change calculation, time labels, and the selected range. These are widget-defined, rather than the original page's fixed five-second refresh and exact rolling 24-hour comparison. The embedded program and data are downloaded separately from this HTML file. The wrapper does not read prices out of the iframe or report quote freshness. The chart area uses a fixed green line; price changes use the widget's gain/loss formatting. TradingView chooses its own initial range when the widget opens; the wrapper does not force a saved range when switching symbols.

## Run locally

Download `tradingview.html` from this branch and open it in a browser, or serve it with any static web server. An internet connection is required to load TradingView.

## Files

`tradingview.html` is this branch's entry point. `index.html` was inherited from `main`; the original Binance version is maintained on `main`.
