# web-scraping-project
Webscraping project for Code Nod Bootcamp.

Hello and welcome,

This project was made to practice creating webscrapers and using API implementation. 

This project in particular was built around the swedish financial forum DI Börssnack and involves two scrapers and two APIs to handle the data scraped. The first scraper simply scrapes the titles of each thread along with the numbers. The scraped information is then sent to OpenAI API with customizable prompts to analyze the text, summarize and condense the information. Then, another prompt converts the summary into a Pandas Dataframe. 

As LLMs can be unpredictable, to ensure you're extracting the right data, the first output will be printed before the DataFrame will. You may need to rerun it a few times before getting satisfactory information.

The DataFrame will also output new information like ticker and list if the subject in question revolves around a listed company, where you can use the small application with InfrontAPI to print a price chart of a chosen stock. You'll need to find the feed, however but it is SSE for swedish stocks not listed on First North or Spotlight Stock Market and NSQ for American Stocks, OSS for norweigan stock etc...

The second scraper will go into every thread individually and extract text from the initial post and every comment, allowing us to analyze the language more closely. This time, there is only functionality for WordCloud. 