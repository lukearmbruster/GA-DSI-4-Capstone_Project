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

  -274,618 posts analyzed  (32% mainstream, 41% fake (mostly from 5 sites
  DcGazette,ThreePercenterNation,     
   DHeadlines,ClashDaily,beforeitsnewscom)
  , 20% conspiracy (mostly from 8 sites CanadaFreePress, ThePoliticalInsider, BradleeDeanSOl,NewsTargetOfficial, 
  freedomoutpost, EyeOpeningInfo, activistpost, TheMindUnleashed), 
  7% satire (mostly from 14 sites TheOnion, clickhole, disclosetv, NewsThump, goingwunderground,elmundotoday,
  WhisperNews, Reductress, HumorTimes, betootaadvocate, CreamBmp, TheCelebricity, TheBeaverton, thehardtimesnews))
  between August 26, 2016
   to January 19, 2017 (includes 73 days before and after the election). 
   -Of all the posts, 98% had links in the posts and 92% had messages. 
    + The top 10 of posting sites (6 mainstream sites and 4 fake sites) make up 37% of the dataset
    + 7,000 more fake news posting (mostly due to DcGazette, ThreePercenterNation, and DHeadlines) occur before the 
      election compared to the period following the election.
      A relatively slight uptick in the number of posts for mainstream after the election compared to before 
      the election (mostly due to yahoonews, usatoday and CBS News).
      There was no noticeable change in the number of posts from conspiracy (although news govtslaves 
      did post about 
      1000 more posts before the election compared to after starting with a post of around 700) and satire pages
      (although goingwunderground did post about 400 more posts before the election compared to after with a 
      post starting around 200). 
    + There is a similar pattern in the number of posts by hour of the day across all types of 
     news sources with a noticable increase including U.S. working hours (4 AM to 7 PM).
    + Proportion of total posts throughout the week remains uniform with the 
     exception of a noticable dip on Saturday and Sunday for all types. 
     types
     + The vast majority of all posts are links for all page types. Videos are second most used post for 
       mainstream, while photo is for fake and conspiracy. 
     
     
   
   -Analyzed a quantities of reactions, shares, and comments (total 900,663,315, including 624,793,478 
   reactions and 275,869,837 shares and comments
    + The top 10 sites with the most reactions make up 75% of the total reactions (6 mainstream, 1 fake, 2 conspiracy, 1  
      satire) 
    + mainstream sites recieved over 300 million more reactions than all other types
    + Most reactions for mainstream site postings came from 4 sites FoxNews, usatoday, ABCNews, and cnn.
      The highest median reactions for a mainstream post came by far from 2 sites FoxNews and usatoday. 
      Most reactions for fake site postings came from 5 sites yesiamright, FreedomDailyNews,DonaldrumpNews.Co,
      supremepatriot, and ClashDaily. The highest median reactions for a fake post came from
      4 sites yesiamright, FreedomDailyNews, supremepatriot, DonaldTrumpNews.Co. 
      Most reactions for conspiracy site postings came from 2 sites ThePoliticalInsider and TheMindUnleashed.
      The highest median reactions for a conspiracy post came from
      4 sites TheMindUnleashed, AwarenessAct, ThePoliticalInsider, and pamelageller.
      Most reactions for satire site postings came from 2 sites TheOnion and disclosetv.
      The highest median reactions for a satire post came from
      5 sites disclosetv, WhispersNews, thehardtimesnews, TheOnion, betootaadvocate. 
    + Much of the increase in the number of reactions occured after the election and was driven by 
      reactions to mainstream posts.
       Mainstream CNN, ABC News, usadtoday, and Fox News had the sizeable increases in 
       reactions after the election, anywhere from 10 million increase to 30 million reaction 
       increase.
       Among fake news, DonaldTrumpNews.Co had the largest change in reactions, which observed a sum reactions
       before the election around 4 million to 13 million reactions. DonalTrumpNews.Co had the most 
       number of reactions out of all fake news. Conspiracy sites had
       the greatest change for ThePoliticalInsider and The MindUnleased (approximately
       a 2 million reduction in reactions after the election and 3 million increase after the
       election, respectively) These pages were also the most popular sites among conspiracy pages as well. 
       The largest change in reactions for satire occured after the election for TheOnion with approximately
       2 million more reactions. The Onion was responsible by far for most of the reactions sums among
       satire pages in general.
    + Mainstream reactions peak between 6 AM and 5 PM, fake between 10 AM to 6 PM,
      conspiracy most uniformly distributed but with a noticable spike at 4 AM to 5 AM, satire between 5 AM to 12 PM
    + At least a 2% reduction in reactions Friday to Monday for Mainstream pages. The remaining types
      do not show as large of a reduction throughout the week, although the next most noticeable reductions
      occur Saturday and Sunday for satire pages. Fake and conspiracy pages appear not to show much of a change
      in the number of reactions throughout the week. 
    + Based on an evaluation of the median, mainstream maintains a relatively high level of uniform engagement over the day,
      and satire has a relatively high level of sustained engagement in the morning with a shorter period in the evening. 
    + Median responses to posts were highest for mainstream and satire posts with a noticeable increase after the 
      election for mainstream news. 
    + All types had at least 2 million more reactions after the election. The largest gain
      occured for mainstream (90 million) followed by fake (12 million), satire (2 million) and 
      conspiracy (2 million)
     + More reactions occur for posts with links for mainstream, fake, and satire pages. Photos are second
     for fake and satire pages, while videos are second for mainstream followed by photo. 
       Conspiracy sites have most of their reactions split between links and photos. 
     MOST IMPORTANT FACEBOOK ENGAGEMENT EDA SUMMARY BELOW 
     + Mainstream posts gather more than 500 million more total engagement actions 
      (reactions, shares, comments) than all other page types. All other page types gather around
      100 million engagement actions or less. In decreasing order, the sum value of engagement
      activities are fake, conspiracy, and satire. 
      for the other 
      + Most engagement actions are likes, followed by shares for all page types. Besides 
        likes the most common reaction type is love for mainstream and haha for satire. 
      + Mean mainstream engagement activities remain 3,000 more than the sum of 
      any engagement activities for other page types. Mean satire and conspiracy engagement
      activities is higher than fake. The standard deviation of the engagement activities
      by type is at least on a scale five times greater than the mean of the engagement
      activities by type. Relatively high standard deviations are observed for number
      of shares for mainstream, conspiracy, and satire, in particular. On a page specific level, standard
      deviation is also higher than mean for sites with relatively high engagement activities. 
      Also on a page specific level, the proportion of shares relative to all other user activities is higher
      for fake, conspiracy, and satire pages compared to mainstream pages. 
      of 
      + 
        
       
      
   
    
    
    
    

    






