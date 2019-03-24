# DataCollection-Using-Webscraping-API
WebScraping and API for data collection
 Scraping Youtube - Matching Videos Details
  Steps:
     (Step 1) : Set Webdriver path for chromedriver accordingly
     (Step 2) : Set Control_key value accordingly. If running on MAC, set Control_key = Keys.COMMAND. If running on
               windows, set Control_key=Keys.COMMAND
     (Step 3) : Using chromedriver, open youtube url
     (Step 4) : Enter search_text as 'Kishore Kumar' and submit page
     (Step 5) : In search results, run a loop 10 times to fetch each video search result details 
     (Step 6) : Open each search result url above, and open video in new window
     (Step 7) : Scroll down the video link to load comments. Check number of comments and load max 50 comments
     (Step 8) : Read below list of values for each video into rowlist
             [href, title, subscriptions,viewsCount, lastUpdated, comments, author, postedTime, replyCount, overallvote]           
     (Step 9) : Create dataframe out of rowlist and columnlist variables above
     (Step 10): Write data from dataframe created above to output_scraping.csv file
  
  
 Scraping Articles using - News API
  Steps:
     (Step1)  : Generate API Key for NewsApiClient
     (Step2)  : Call newsapi.get_everything with query q as 'business analytics' and sort_by='publishedAt' to sort 
               by recent ones
     (Step 3) : In response returned, check totalResults returned to find number of matching articles
     (Step 4) : newsAPI returns 20 articles per page. So, in results returned, loop through        totalResults/defaultPageSize times. Note, defaultPageSize = 20
     (Step 5) : Each time in for loop, read fields - source id, source name, author, title, description and content
     (Step 6) : Write above article fields to articleRow
     (Step 7) : Append each of the articles to articleList
     (Step 8) : newsapi limits number of matching article responses to 1000 (till Page=50)
     (Step 9) : Convert articleList to dataframe object
     (Step 10): Write articleDF object to output_api file
