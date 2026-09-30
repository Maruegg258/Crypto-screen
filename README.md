# Crypto Screen

A compact, dark-themed monitor for Binance USDⓈ-M perpetual futures:

- BTC / USDT
- ETH / USDT
- HYPE / USDT
- Latest trade price refreshed every 5 seconds
- Rolling 24-hour interactive line charts
- 24-hour price and percentage changes
- Hourly time ticks in Asia/Taipei
- Numeric highlights for the current and 24-hour reference prices
- Pointer and touch inspection for exact time and price
- Background updates pause while the page is hidden

## Run locally

Open `index.html` in a browser, or serve the repository with any static web server.

## TradingView tab view

Open [`tradingview.html`](tradingview.html) for the compact TradingView version:

- BTC, ETH, and HYPE tabs above a single Symbol Overview widget
- Binance USDT perpetual contracts (`BINANCE:BTCUSDT.P`, `BINANCE:ETHUSDT.P`, `BINANCE:HYPEUSDT.P`)
- Dark theme, price and percentage change, a one-day area chart, right-hand price scale, and pointer inspection
- TradingView attribution and a direct link to the selected contract
- Keyboard tab navigation and a retry button if the embed cannot load
- One selected widget at a time; switching symbols removes the previous embed

This is a standalone HTML file with no build step, framework, API key, or backend. TradingView supplies the embedded market data and controls its update frequency, availability, change calculation, time labels, and 1D range. These are widget-defined, rather than the original page's fixed five-second refresh and exact rolling 24-hour comparison. The embedded program and data are downloaded separately from this HTML file. The wrapper does not read prices out of the iframe or report quote freshness. The chart area uses a fixed green line; price changes use the widget's gain/loss formatting.

## GitHub Pages

In the repository, open **Settings → Pages**, select **Deploy from a branch**, then choose **main** and **/(root)**.

## Data

The page reads public Binance USDⓈ-M Futures market endpoints directly from the visitor's browser. No API key or backend service is required.

When Pages is enabled, append `/tradingview.html` to this repository's Pages URL to open the TradingView version. The HTML can also be opened directly after downloading it.
