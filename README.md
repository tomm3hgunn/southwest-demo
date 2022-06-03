# Southwest Fare DEMO
This repo does not include source code and is used for demo purposes only. It will visually present the functions of my southwest fare program.

## Description
Automate checking for prices for Southwest flights. By giving an origin, destination, and the leaving/returning dates, get email updates on the prices when they drop/rise. Utilizing the Selenium library to automate filling in the forms and scraping the data.

Utilizes SQL database to store and receive data in order to compare current and previous prices. Selenium is used to crawl through the initial forms that lead to the prices and dates. Once at the desired webpage, the selenium driver is closed and lxml is used to scrape the received webpage. smtplib is then used to email notifications to a recepient when a price change is discovered. A price is checked every hour using the ischedule library and runs in the background on a linux machine.

In main.py, it runs a full scan of a chosen origin/destination calendar. In SinglularTrack.py, the link is hardcoded to a specific page to get a single price change where the flight is non-stop.

Data is visualized with matplotlib to display a graph of a full calendar for a specific origin/destination to depart/return dates. History graphs of every single date for a specific origin/destination is generated.
