# Extracting and Visualizing Stock Data

This project uses Python to extract, clean, and visualize historical stock price and revenue data for **Tesla (TSLA)** and **GameStop (GME)**. The goal is to identify trends and compare financial performance against market sentiment, specifically focusing on the volatile period leading up to mid-2021.

## Table of Contents

* [Overview](#overview)
* [Installation](#installation)
* [Data Sources](#data-sources)
* [Project Structure](#project-structure)
* [Visualizations](#visualizations)
* [Key Insights](#key-insights)

## Overview

This notebook performs the following tasks:

1. **Stock Data Extraction**: Uses the `yfinance` library to pull historical share prices.
2. **Revenue Data Web Scraping**: Uses `BeautifulSoup` and `pandas` to scrape quarterly revenue tables from web sources.
3. **Data Cleaning**: Processes strings, removes unwanted characters (like `$` and `,`), and handles missing values.
4. **Data Visualization**: Generates side-by-side comparison graphs of stock prices vs. company revenue.

## Installation

To run this notebook, you will need Python installed along with the following libraries:

```bash
pip install yfinance pandas requests beautifulsoup4 html5lib lxml matplotlib

```

## Data Sources

* **Stock Prices**: Extracted directly from Yahoo Finance via the `yfinance` API.
* **Revenue Data**: Scraped from historical financial data pages hosted on IBM Developer Skills Network.

## Project Structure

The notebook is organized into the following sections:

* **Tesla Analysis**: Extraction of TSLA stock data and web scraping of TSLA revenue.
* **GameStop Analysis**: Extraction of GME stock data and web scraping of GME revenue.
* **Graphing Function**: A custom `make_graph` function that creates a two-panel plot showing share price and revenue on a shared timeline.
* **Dashboarding**: Plotting the results to visualize the correlation (or lack thereof) between price and earnings.

## Visualizations

The project includes a `make_graph` function that:

* **Top Panel**: Displays the "Historical Share Price" in blue.
* **Bottom Panel**: Displays "Historical Revenue" in green.
* **Zoom Tool**: The graphs are automatically focused on data leading up to June 2021 to highlight specific market events.

## Key Insights

The visualization highlights a significant observation regarding the **2021 GameStop short squeeze**:

* While GameStop's stock price skyrocketed to record highs in early 2021, its actual revenue was hitting a long-term low.
* This visual analysis proves that the price surge was driven by market technicals and investor sentiment rather than the company's fundamental financial growth.