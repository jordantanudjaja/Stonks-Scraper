# Stonks-Scraper

A personal project that tracks my personal investments and scrapes the internet for information on securities (stocks and funds) and cryptocurrencies. The idea of this project is to evaluate and compare different securities and cryptocurrencies with each other and find good sources of investments through the concept of value investing. The entire information is scraped using functions in Google Sheets and Google Script due to its interactivity with Google Finance API. Additional functions in Google Sheets (IMPORTHTML and IMPORTXML) are used to supplement the web scraping process by scraping information that is not found in Google Finance from other financial tracking websites.

This is a personal project on creating a personal yugioh toolkit that allows anyone to access any yugioh card and see 
its information conveniently. I noticed that the yugioh wiki website: https://yugioh.fandom.com is not particularly
user-friendly, especially when it comes to searching multiple cards through certain filters. The URLs of certain cards
are missing when clicking on the next page button, and it takes a lot of time and effort to access a particular card in
this way. This project is an attempt to alleviate this problem by scraping the entire website for all its card URLs and
making my own personal card database. The toolbox will not only feature the entire Yugioh Card Database, but also functionalities
that:
1) Updates the database based on new cards being added to the game
2) Updates the competitive status of each card in the database from the most recent banlist
3) Provides an interactive platform that searches the prices of cards I am interested in buying

Potential idea expansion: Deck-building toolkit, server-side capabilities through Django, and machine learning functions that shows
which card I am interested in based on my previous purchases.

<b>Websites Scraped:</b>
<ol>
    <li>https://yugioh.fandom.com</li>
    <li>https://www.yugioh-card.com/uk/gameplay/detail.php?id=1155</li>
    <li>https://www.tcgplayer.com</li>
</ol>

<h1>yugioh Project Directory</h1>
<h2>yugioh Package</h2>
<h3>Modules</h3>
<ul>
    <li><b>__init__:</b> Initialization Module</li>
    <li><b>ygfandom:</b> Module containing classes to view and make changes to the Yugioh Card Database.csv or the
    backup csv file through web scraping the website: https://yugioh.fandom.com</li>
    <li><b>banlist:</b> Module containing the banlist_update function that scrapes the website:
    https://www.yugioh-card.com/uk/gameplay/detail.php?id=1155 and updates the card database according to the most
    recent banlist</li>
    <li><b>tcgplayer:</b> Module containing classes that scrapes the website: https://www.tcgplayer.com and searches
    the current card prices of cards the user is interested in buying and returns pre-defined price statistics</li>
</ul>
<h3>Unit Tests</h3>
<ul>
    <li><b>pytest.ini:</b> File to setup user-defined markers for each testing function</li>
    <li><b>test_ygfandom:</b> Testing file to test the classes in the ygfandom module</li>
    <li><b>test_banlist:</b> Testing file to test the banlist_update function in the banlist module</li>
    <li><b>test_tcgplayer:</b> Testing file to test the classes in the tcgplayer module</li>
</ul>

<h2>Data</h2>
<ul>
    <li><b>Yugioh Card Database.csv:</b> CSV file that contains 99% of Yugioh cards up to the current Link format</li>
    <li><b>Yugioh Card Database (Backup).csv:</b> Same csv file as Yugioh Card Database.csv that serves as a backup
    file in case something happens to the original file</li>
    <li><b>Yugioh Card Database (Testing).csv</b> Same file as Yugioh Card Database.csv that serves as the Testing
    Database Control File for the Unit Testing Procedures</li>
</ul>

<h2>External Applications</h2>
<ul>
    <li><b>chromedriver.exe:</b> ChromeDriver executable app that works with the Selenium Python module to scrape dynamic websites
    such as https://www.tcgplayer.com</li>
</ul>

<h2>Jupyter Notebooks</h2>
<ul>
    <li><b>Analytics and Checkup:</b> Notebook platform for doing quality checkup on the card database and doing any type of
    data analysis, visualization and editing or updating card data</li>
    <li><b>Card Database Initialization:</b> First notebook created to initialize the Yugioh Card Database.csv file. It contains
    functions that were used to scrape the https://yugioh.fandom.com for card sets (packs, decks, collectible tins etc) urls
    and grab each card's information and store it in a DataFrame format</li>
    <li><b>Card Price Toolbox:</b> Notebook platform to analyze and compare different card prices and provide a shopping cart
    for users to make purchasing decisions. Potential expansion includes a deck building toolbox embedded in this notebook</li>
</ul>

<h2>setup.py</h2>
<p>Setup file that is used to make this yugioh project directory as the root directory and the yugioh package an actual local
Python Package. This allows modules to be imported interchangeably in jupyter notebooks and python scripts without incurring
an Import or ModuleNotFound Error</p>

<h2>yginterface.py</h2>
Python Script that provides the user with an interface to interact with the Yugioh Card Database. It has 7 functions:
<ol>
    <li>Updating new cards to the database individually or in small amounts using their own unique URL</li>
    <li>Updating new cards to the database through a card set URL, such as booster pack or structure decks</li>
    <li>Updating the competitive status of the cards through cross-referencing with the current banlist</li>
    <li>Doing a regulatory checkup and seeing if there are any errors in adding new cards or if
    there is a need to update status of existing cards </li>
    <li>Checking current prices of any Yugioh card (even those not in the Yugioh Card Database)</li>
    <li>Checking the current prices of a card/cards that are only in the current Yugioh Card Database</li>
    <li>Planning a shopping cart for purchasing cards in the current Yugioh Card Database</li>
</ol>
