# web-scraping

Extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. You’ll scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.

## What You're Creating

The challenge consists of :

1. Scrape titles and preview text from Mars news articles.
2. Scrape and analyze Mars weather data, which exists in a table.

## Instructions

## Part 1: Scrape Titles and Preview Text from Mars News

1. Use automated browsing to visit the Mars news site (<https://static.bc-edx.com/data/web/mars_news/index.html>). Inspect the page to identify which elements to scrape.
2. Create a Beautiful Soup object and use it to extract text elements from the website.
3. Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:

    * Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview.
    * Store all the dictionaries in a Python list.
    * Print the list in your notebook.
4. Optionally, store the scraped data in a file. o do so, export the scraped data to a JSON file.

## HINT

To identify which elements to scrape, you might want to inspect the page by using Chrome DevTools.

## Part 2: Scrape and Analyze Mars Weather Data

1. Use automated browsing to visit the Mars Temperature Data Site (<https://static.bc-edx.com/data/web/mars_facts/temperature.html>). Inspect the page to identify which elements to scrape.
2. Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.
3. Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:

    * id: the identification number of a single transmission from the Curiosity rover
    * terrestrial_date: the date on Earth
    * sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
    * ls: the solar longitude
    * month: the Martian month
    * min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
    * pressure: The atmospheric pressure at Curiosity's location
4. Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
5. Analyze your dataset by using Pandas functions to answer the following questions:

    * How many months exist on Mars?
    * How many Martian (and not Earth) days worth of data exist in the scraped dataset?
    * What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
        * Find the average minimum daily temperature for all of the months.
        * Plot the results as a bar chart.
    * Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
        * Find the average daily atmospheric pressure of all the months.
        * Plot the results as a bar chart.
    * About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
        * Consider how many days elapse on Earth in the time that Mars circles the Sun once.
        * Visually estimate the result by plotting the daily minimum temperature.
6. Export the DataFrame to a CSV file.

## References

The Mars News website (<https://static.bc-edx.com/data/web/mars_news/index.html>) is operated by edX Boot Camps LLC for educational purposes only. The news article titles, summaries, dates, and images were scraped from NASA's Mars News website in November 2022 (<https://mars.nasa.gov/>). Images are used according to the JPL Image Use Policy(<https://www.jpl.nasa.gov/jpl-image-use-policy>) , courtesy NASA/JPL-Caltech.
