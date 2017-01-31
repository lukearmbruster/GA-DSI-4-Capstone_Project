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

  -274,618 posts analyzed  (32% mainstream, 41% fake, 20% conspiracy, 7% satire) between August 26, 2016
   to January 19, 2017 (includes 73 days before and after the election). 
    + The top 10 of posting sites (6 mainstream sites and 4 fake sites) make up 37% of the dataset
    + 7,000 more fake news posting (mostly due to DcGazette, ThreePercenterNation, and DHeadlins) occur before the 
      election compared to the period following the election.
      A relatively slight uptick in the number of posts for mainstream after the election compared to before 
      the election (mostly due to yahoonews, usatoday and CBS News).
      There was no noticeable change in the number of posts from conspiracy (although govtslaves did post about 
      1000 more posts before the election compared to after with a post of around 700) and satire pages
      (although goingwunderground did post about 400 more posts before the election compared to after with a 
      post of around 200). 
    + There is a similar pattern in the number of posts by hour of the day across all types of 
     news sources with a noticable increase including U.S. working hours (4 AM to 7 PM).
    + Proportion of total posts throughout the week remains uniform with the 
     exception of a noticable dip on Saturday and Sunday for all types. 
     types
     
   
   -Analyzed a total of 624,793,478 reactions 
    + The top 10 sites with the most reactions make up 75% of the total reactions (6 mainstream, 1 fake, 2 conspiracy, 1  
      satire) (mainstream sites recieved over 300 million more reactions than all other types)
    + Mainstream reacions peak between 6 AM and 5 PM, fake between 10 AM to 6 PM,
      conspiracy most uniformly distributed but with a noticable spike at 4 AM to 5 AM, satire between 5 AM to 12 PM
    + At least a 2% reduction in reactions Friday to Monday for Mainstream pages. The remaining types
      do not show as large of a reduction throughout the week, although the next most noticeable reductions
      occur Saturday and Sunday for satire pages. Fake and conspiracy pages appear not to show much of a change
      in the number of reactions throughout the week. 
    + Based on an evaluation of the median, mainstream maintains a relatively high level of uniform engagement over the day,
      and satire has a relatively high level of sustained engagement in the morning with a shorter period in the evening. 
    + All types had at least 2 million more reactions after the election. The largest gain
      occured for mainstream (90 million) followed by fake (12 million), satire (2 million) and 
      conspiracy (2 million)
     + 
      
   
    
    
    
    

    






