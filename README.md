# Scraping_for_list_of_hotels


# Gspreadhotelscraper


Goal: To scape the website yatra.com for the list of hotels in a particular city.
City: Jaipur
Libraries used: Selenium, pandas, df2gspread, oauth2client
Challenges faced: Chromedriver was not compatible with the current updated Chrome version (Version 117.0.5938.89). The latest one they had was ChromeDriver 114.0.5735.90 and it only supported Chrome version 114. I had to search for a bit to figure out how this could be fixed.
The ChromeDriver that is compatible with the updated version of Chrome is still in the testing phase, so I had to choose the right stable version for that and after working on it for a while, I was able to make it work.

Process: 

1: Using Selenium and Chrome webdriver, scraped the first 10 pages of the website.
2: Data scraped: Hotel, City, Rating, Price
3: Performed Data Pre-processing
4: Converted the scraped data into a Data Frame using Pandas
5: Logged into console.developers.google.com to get the required APIs for Google Drive and for Google Sheets. Created private key in JSON file format (This file is useful as it provides clients email that will be used to link our code with Google Spreadsheet.
6: Using the df2gspread library, uploaded the data to Google Spreadsheet.
