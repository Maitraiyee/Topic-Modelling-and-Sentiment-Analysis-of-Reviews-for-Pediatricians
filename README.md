# Text Analytics on Pediatricians

## Objective

An increasing number of doctor reviews are being generated by patients on the internet. These reviews address
a diverse set of topics (features), including wait time, office staff, doctor’s skills, and bedside manners. Most previous work on
automatic analysis of Web-based customer reviews assumes that (1) product features are described unambiguously by a small
number of keywords, for example, battery for phones and (2) the opinion for each feature has a positive or negative sentiment.
However, in the domain of doctor reviews, this setting is too restrictive: a feature such as visit duration for doctor reviews may
be expressed in many ways and does not necessarily have a positive or negative sentiment. Our objective was to 
identify key aspects on which pediatricians are reviewed or rated on different healthcare websites like RateMD and HealthGrads. 

## Description

We have taken Pediatricians around the State of Illinois for our project from two websites namely Healthgrades and Ratemds. Performed web scraping to extract the reviews and doctor demographics with the help of Python’s exclusive 
Selenium library. Along with the reviews, Doctor demographics like Name, Age, Years of experience, etc. are also being extracted. 

Taking doctor demographics in account 
we performed sentiment analysis review wise for each doctor to assess the sentiment scores by breaking up the reviews into meaningful phrases using tool called VADER.
VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media.

As a result of the Sentiment analysis we calculated total number of positive, negative and neutral sentiments. The Positive, Negative and Neutral scores represent the proportion of text that falls in these categories

Threshold used : 

 Greater than 0  0 - positive 
 
 Less than  0 – negative
 
 Rest Neutral
 
 Analysis of long-term doctor reviews gave us the common domains on which doctors are reviewed namely:
 
 Communication skills
 
 Medical Expertise
 
 Time spent & Scheduling
 
 Bedside manners
 
 Costs
 
 Office staff & Environment
 
 As mentioned earlier our objective was to analyze the how the pediatricians are reviewed on the above aspects. For that we made use of the Sentiment analysis results for the reviews
 broken into phrases. We performed an improvised version of topic modelling named "Semi-Supervised approach" using CorEx algorithm. CorEx a semi-supervised topic model that — unlike LDA, allowed us to provide the model with 
 “anchor words” that represented potential topics we thought the model should attempt to find. Before implementing the CorEx algorihm, we removed the phrases with neutral 
 sentiment scores as it will not make any sense in performing topic modelling in it. We used our Bag of words themes as “Anchor words” for semi-supervised learning with weight value as 3.
 From the CorEx results, we calculated the total number of phrases per doctor and calculated the average score(number of phrases in each theme/total) for each theme per doctor. Now we have 12 new independent variables for our analysis.
 
 Finally, with the star rating extracted from online being dependent variable and Review characteristics , the aspect-based scores and doctor demographics as Independent variable we performed
 Statistical analysis followed by a Linear regression to identify key influential factors affecting the overall rating for a doctor. 
 
 ## Findings
 
Primarily, themes like communication, costs and office staff having a negative review can impact the star rating.

Higher the average words per review, the rating and overall sentiment is affected negatively.

Gender has no influence on the rating of the pediatrician. Therefore, the ratings of pediatricians are gender neutral.

Overall positive sentiment increases with years of experience.

Technology: Text Analytics, NLP, Regression, Web Scraping, Python, Excel






 


