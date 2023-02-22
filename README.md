# Web Scraping for Tennis Data

This repository contains a collection of scripts/notebooks for scraping tennis event data from the ATP, Australian Open and Roland Garros Infosys Match Centre/Court Vision pages. 

## Project Information

The original motivation for this repository/project was to scrape tennis serve data from the court-vision pages of each match. I initially came to know about these dashboards through Peter Tea's [tennis serves project](https://github.com/petertea96/tennis_analytics/tree/master/projects/roland_garros_project). Late last year I found out that several ATP tournaments started having them and decided to give extracting the locational service data a go. As the raw data is encrypted, my first workaround solution was a convoluted selenium-based code that clicked every visible point on the court vision timeline. Some time passed before I came across this [originally JS solution](https://stackoverflow.com/questions/73735401/scraping-an-atptour-com-api-returns-what-looks-like-encrypted-data), which has greatly simplified the code now to be able (a.o. Feb 2023) to extract and decrypt the actual raw court vision data (which contains much more information than just the serves/winners). 

## `api-info/`
Contains API information from each tournament that Infosys provides the court vision application for (Australian Open, Roland Garros, ATP). 

## `figures/`
Contains several example figures that were created throughout the exploratory part of this project.

## `notebooks/`
Contains the various scraping codes in Jupyter Notebook (`.ipynb`) format. 

- Notebooks with "`_Tournaments_`" demonstrate scraping tournament (match results, player list) information into CSV format. 

- Notebooks with "`_Court-Vision-Raw_Scraper`" scrape and decrypt the raw data into JSON format. 

- Notebooks with "`_old`" include the original selenium-based code. 
