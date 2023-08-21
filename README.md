## PWC-Call-Centre-trends-dashboard

# Table of Content:
+ Problem Statement
+ Data Source
+ Data Preparation
+ Data Visualization
+ Insights


# Problem Statement:
I was given a task to Create a dashboard in Power BI that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

+ Possible KPIs include (to get you started, but not limited to):
- Overall customer satisfaction
- Overall calls answered/abandoned
- Calls by time
- Average speed of answer
- Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

# Data Source: 

# Data Preparation:
Created required measures using DAX 

+ Total Calls = `COUNT(Sheet1[Call Id])`
+ Answered Calls = `COUNTX(FILTER('Sheet1' , 'Sheet1'[Answered (Y/N)] = "Y") , 'Sheet1'[Call Id])`
+ Unanswered calls = `COUNTX(FILTER('Sheet1' , 'Sheet1'[Answered (Y/N)] = "N"), 'Sheet1'[Call Id])`
+ Resolved issues = `COUNTX(FILTER('Sheet1', 'Sheet1'[Resolved] = "Y"), 'Sheet1'[Answered Calls])`
+ Unresolved issues = `COUNTX(FILTER('Sheet1', 'Sheet1'[Resolved] = "N"), 'Sheet1'[Call Id])`
+ Avg. speed of answer = `AVERAGE('Sheet1'[Speed of answer in seconds])`
+ Avg. Talk Duration = `FORMAT(AVERAGE('Sheet1'[AvgTalkDuration]) , "HH:MM:SS")`


# Data Visualization:

![b](https://github.com/Ananya-Foujdar05/PWC-Call-Centre-trends-dashboard/assets/140806083/1e9f008c-51fe-4ef2-b2c1-035779db68fb)

![c](https://github.com/Ananya-Foujdar05/PWC-Call-Centre-trends-dashboard/assets/140806083/d21a9d4f-182c-47b8-b742-129cf897a2b5)


# Insight:
+ The majority of calls were successfully answered, ensuring great customer service satisfaction.
+ Interestingly, the number of calls gradually decreased each month, indicating potential areas for improvement in call volume management.
+ Customers seem to be generally satisfied, with the most ratings are 3 and 4.
+ Streaming-related calls dominated the call center activity, suggesting a trending topic in customer inquiries.On the other hand, contract-related calls were the least frequent.
+ Highest number of calls answered and issues resolved by Jim.
+ Joe has the highest average speed of answer in second.
+ Martha has the highest average satisfaction rating.


