# Stonks-Scraper

A personal project that tracks my personal investments and scrapes the internet for information on securities (stocks and funds) and cryptocurrencies.
The idea of this project is to evaluate and compare different securities and cryptocurrencies with each other and find good sources of investments
through the concept of value investing. The entire information is scraped using functions in Google Sheets and Google Script due to its interactivity
with Google Finance API. Additional functions in Google Sheets (IMPORTHTML and IMPORTXML) are used to supplement additional data by scraping
information that is not found in Google Finance from other financial tracking websites.

Potential idea expansion: Apply ML techniques to do some form of technical analysis to predict future value, Monte Carlo simulation and solver analysis
to apply the CAPM model to find best portfolio combination with highest potential returns and lowest risk (variance).

<b>Websites Scraped:</b>
<ol>
    <li>https://www.google.com/finance/</li>
    <li>https://finance.yahoo.com/</li>
    <li>https://finviz.com/</li>
    <li>https://www.marketwatch.com/</li>
</ol>

<b>Other Websites Referenced:</b>
<ol>
    <li>https://companiesmarketcap.com/</li>
    <li>https://coinmarketcap.com/</li>
    <li>https://www.coingecko.com/en</li>
</ol>    

<h2>Google Sheets</h2>
<h3>Portfolio Tracker</h3>
<ul>
    <li><b>URL:</b> https://docs.google.com/spreadsheets/d/1xHJSsDsQEu_YvFmtNnefFBv3l1AatDd34L3f9680ehw/edit?usp=sharing</li>
    <li><b>Description:</b> This Google Sheet tracks my personal investments and contains the overall portfolio summary (with data visualizations) and
    the ledger that contains my buying and selling transactions. This sheet also has a Google Script attached to it that automates my position
    for each security and cryptocurrency every time I update the sheet with a new transaction.</li>
</ul>
<h3>Stocks Watchlist</h3>
<ul>
    <li><b>URL:</b> https://docs.google.com/spreadsheets/d/14-HaYDTdRZCm35_TGx1MhRNTvZ4pdAkWsvSeFonsn8k/edit?usp=sharing</li>
    <li><b>Description:</b> This Google Sheet scrapes information about various stocks, and organized it based on their sectors. The Control Panel tab
    dictates which sector of stocks will be viewed based on user choice, and the Stocks Analyses tab display the list of stocks that matches
    the sector choice and the stocks' associated information, supported with data visualizations.</li>
</ul>    
<h3>Mutual Funds & ETFs Watchlist</h3>
<ul>
    <li><b>URL:</b> https://docs.google.com/spreadsheets/d/1_n4wkzUW12aMnJ4ylxtGIIoe_28wbvNboaYgsTpP_NQ/edit#gid=1108658010</li>
    <li><b>Description:</b> This Google Sheet scrapes information about various mutual, index, and exchange-traded funds and organized them based on
    their type (Equity, Money Market, etc), and sub-type (Large-cap, sector-based, etc). The Control Panel tab dictates which
    umbrella of funds will be viewed based on user choice, and the Funds Analyses tab display the list of funds that matches that filter choice
    and the fund's associated information, supported with data visualizations. The Deep Dive tab scrapes information about a chosen fund's portfolio
    and its exact distrbution of securities. This sheet also has a Google Script attached to it that serves to dynamically change the bordering of
    the tables on the Deep Dive tab whenever the fund ticker is changed.</li>
</ul>
<h3>Cryptocurrency Watchlist</h3>
<ul>
    <li><b>URL:</b> https://docs.google.com/spreadsheets/d/1Im9RHEw4SuJtp0CGzYKQ5IBbHtQELkQ3jHf_K6U_X0E/edit?usp=sharing</li>
    <li><b>Description:</b> This Google Sheet scrapes information about various cryptocurrencies and display their associated information, supported with
    data visualizations. This sheet also has a Google Script attached to it that automatically sorts the crypto tickers according to their market
    capitalization value in ascending order.</li>
</ul>
<h3>Fundamental Analysis Calculator</h3>
<ul>
    <li><b>URL:</b> https://docs.google.com/spreadsheets/d/1-T7eJD7CyP8tuYGM0ZH2u-7fR4lPVP3Rdh_E1Ajfa_8/edit?usp=sharing</li>
    <li><b>Description:</b> This Google Sheet scrapes information about a company's financial statements and calculates its intrinsic value based on certain
    assumptions through various models (DCF, DDM, and EPS). The purpose of this sheet is to determine the valuation of a stock based on a reasonable
    margin of safety and help me decide if a particular stock is a good buy or not.</li>
</ul>
<h3>Specific Security Historical Data</h3>
<ul>
    <li><b>URL:</b> https://docs.google.com/spreadsheets/d/1urDssKdHILGDmiq0t73WDQ6UpOyMQ5kUhSggMdn4oBc/edit?usp=sharing</li>
    <li><b>Description:</b> This Google Sheet scrapes the Google Finance API for any security in its database and pulls the historical closing prices of that 
    security for the past 5 years or from any date I desire. This sheet is used in conjunction with the Time Series Analysis using fbprophet jupyter notebook 
    to forecast future prices of any security.</li>
</ul>

<h2>Jupyter Notebooks</h2>
<h3>Machine Learning Analysis</h3>
<ul>
    <li><b>Time-series Analysis using fbprophet.ipynb:</b> A notebook that utilizes the fbprophet library to forecast future data on a security based on its 
    historical data, taking into account seasonality in the calculations.</li>
</ul>
