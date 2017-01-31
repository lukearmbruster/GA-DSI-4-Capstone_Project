# GA-DSI-4-Capstone_Project

January 24, 2017

Goals:

1. Articulate specific aim

  My aim in this project is to identify what factors contribute to high user engagement 
  on mainstream and fake news pages as measured by Facebook reactions. Once the factors 
  are identified, build a model that predicts whether a news source is fake or mainstream, 
  and build another model that determines which topics are likely to be most popular among
  followers. 

2. Outline proposed methods and models

  -Via the Facebook Graph API, download post features of fake and mainstream news sources as 
   identified by published sources. Desired post features include id, message, link name, 
   post type (i.e. event, link, photo, status, video), post link, date published, count of 
   reactions, count of comments, count of shares, count of likes, count of loves, count of 
   wows, count of hahas, count of sads, and count of angrys. Download post features approximately 
   two months before and after the U.S. presidential election to evaluate the possible effect of 
   a major political event on news coverage. 
   
   -Remove any repeating posts
   
  -Determine the relationships between the posts and reactions through exploratory data analysis 
   (i.e. plotting, applying statistical analysis, and vectorizing n-grams in post messages and link 
   names for fake and mainstream news).
   
  -Build supervised models with interpretable feature effects (e.g. linear, logistic regression). 

3. Define risks and assumptions

  -Subjective designation of fake and mainstream news sources
  
  -Fake and mainstream news sources included in the analysis may not be representative of all 
   mainstream and fake news sources

4. Describe data cleaning/munging techniques

  -Conversion between unicode and ascii
  
  -Adding stop words in n-gram vectorizer analysis

5. Summary of EDA

  -274,618 posts analyzed  (41% fake, 32% mainstream, 20% conspiracy, 7% satire)
    + The top 13% of posting sites (4 fake sites and 6 mainstream sites) make up 53% of the dataset
  
  -Mainstream pages generate at least 20 million more total reactions each day of the week 
   over the study period compared to fake news. Most user engagement falls between 10 am 
   and 5 pm on fake news pages and between 8 am and 5 pm on mainstream pages
  
  - Mainstream news pages post a similar number of posts as fake news pages each hour of 
    every day and week day. A similar hourly and daily posting pattern is observed among 
    mainstream and fake news pages. Saturday shows the lowest number of posts with each day further from Saturday showing
    gradually more posts. 7 am and 5 pm peak posting time for fake news and mainstream
    news both before and after the election. A similar daily post count pattern is 
    observed before and after the election. The number of postings was similar for 
    both before and after the election for mainstream and fake news pages, respectively.
    The number of postings was also similar between mainstream and fake news.
  
  -The most common type of post among news pages includes a link, followed by photo
   and video.
  
  - DCGazette had nearly twice as many posts as the nearest highest fake news poster.
    Fox news is getting by far the highest number of total number of reactions.
    DonaldTrumpNews.Co gets the highest number among reactions among fake news.
   
   -The highest poster among mainstream is yahoo news, followed closely by usatoday.
    The highest poster among fake news   is by far DcGazette. 
    
    






