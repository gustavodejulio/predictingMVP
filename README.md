This project is scraping all the info from baskteball-reference.com to analyze and predict the MVP of the next season based on the stats from (1991-2021).

Scraping lib:
Requests: used to get simple pages information, content is the whole page
BeautifulSoup: get the raw information from the html file
Selenium:  uses a webserver to get info from a website that uses JavaScript to load the full content
Pandas: manipulation/store

Machine Learn:
On this part we cleaned more the data to fit properly the ML model, first we used Ridge Regression.
To find the error between the predicton and the real rank, we created a backtest function that check where the first 5 predictions are and how far they are from the real rank. Ex: if the predict stats says that one guy is going to be on the top 5 of the mvp running and he is there, we get full points, the penalty goes to how far is the real number to the prediction, so we sum all and divide by the lenght.

With Ridge Regression we got a 72.12%
With Random Forest we 74
