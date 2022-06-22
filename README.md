# Capstone_Project_NSS

Sentiment Analysis of r/Teachers Posts

Capstone Project for Cohort DA6 at Nashville Software School

Contents
Motivation
Data Sources and Tools
Data Analysis
Challenges
Conclusions

Motivation

I worked as a teacher and librarian in public schools for 15 years prior to enrolling in Nashville Software School’s Data Analytics program. Throughout my time in education there was a common sentiment amongst teachers that the public education system in our country has changed for the worse over the last 10-15 years. While the state of our current education system is complex, with many complicated factors that help explain how we got to where we are, I wanted to focus on teachers’ perception of education. Unfortunately the surveys that are available are not standardized so I chose to focus on online posts.

Back to Contents

Data Sources and Tools

Data Sources

Teacher Posts: Accessed top posts on the subreddit r/Teachers using PushShift API
Teacher Salary Data: NEA Research and Publications

Tools

Python/Jupyter Notebooks for retrieving and analyzing data
Tableau for data visualization

Back to Contents

Data Analysis

For my analysis I used Python to create dataframes for the top 1000 posts in the r/Teachers subreddit (as determined by the number of upvotes) for 2014 - 2022. I then used VADER (Valence Aware Dictionary and sEntiment Reasoner) from the Natural Language Toolkit to categorize each post as positive, neutral, or negative and assign a sentiment score. I then calculated some descriptive statistics to find the mean and median for each year. Finally, I used WordCloud to create a word cloud showing the top 100 words from all dataframes. I wanted to see if there was any correlation between teacher salaries and their sentiment so I pulled data from NEA’s Research and Publications to analyze the overall average for the United States as well as the top 10 and bottom 10 states for teacher pay. I then added all of this information to Tableau to create visualizations of the data. 

Back to Contents

Challenges

I initially wanted to use Twitter’s API to look at post using #education however their API is limited to only 7 days so I wasn’t able to look at posts over time. 

I pivoted to r/Teachers and ran into a similar issue with Reddit’s API. However, there is an alternative API run by developers, PushShift, that allowed me to pull posts using timestamps. Unfortunately there were still some limitations with this method. My goal was to pull the top 1000 posts per year as determined by the number of upvotes. Unfortunately the PushShift API gave repeated “shards down” warnings that affected the integrity of some of my data and not all years returned exactly 1000 posts. 

Back to Contents

Conclusions

Dashboard: Analysis of Teacher Sentiment Towards Education 

I created the dashboard above to analyze the sentiment scores. The only significant change in teacher sentiment came between 2020 - 2022. During this time the average score dropped from .31 to .12, whereas it has previously only moved from .25 to .31. There did not appear to be any correlation between that score and teacher sentiment.



These are the top 100 words used in the top posts for all years.

Teacher salary has remained relatively stagnant over time. The top paying areas ten to be in New England and the bottom salaries seem to be mostly in the south. There doesn’t appear to be a correlation between salary and teacher sentiment. 
