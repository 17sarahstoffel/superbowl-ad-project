# superbowl-ad-project

#### Contributors (Group 4)
Armand Dauti, Alan Jallah, Sarah Stoffel, Scott Neubauer

## Synopsis
In this project we examined the rewatchability and topic distribtion of televised ads over the past 20 Superbowls (2000 - 2020). Our dataset was found on [GitHub](https://github.com/fivethirtyeight/superbowl-ads) and was used in an [article](https://projects.fivethirtyeight.com/super-bowl-ads/) by FiveThirtyEight.

## Process
Our first task was to import and clean the data from our dataset then import and clean the data from the YouTube Data v3 API. We used Pandas methods for the importing and cleaning of the original dataset (.csv file) and 'requests.get' to retrieve the YouTube analytics in JSON format. The YouTube data contained some empty records as some of the linked videos were either deleted or set to Private by the uploader. To get around this, we had to remove the records associated. Once the data was cleaned and organized, we moved on to answering the following questions.

## Questions
1. What was the distribution of ad categories by count and YouTube view counts per ad tag over the past 20 years?
	* This was addressed by separating and counting the relevant data using Pandas then plotting it with MatPlotLib bar charts.
2. What was the distribution of ad counts and YouTube views when separated by when the 'Funny' tag is True or False?
	* This was addressed by separating and counting the relevant data using Pandas then plotting it with MatPlotLib pie charts.	
3. Were videos tagged as 'Funny' viewed more in YouTube than their 'Not Funny' counterparts?
	* This was addressed by extracting the view count data according to whether or not an ad was tagged with the 'Funny' category. Two series were created then a Chi Square test was performed. This is expanded upon later.
4. How has ad length varied over the past 20 years?
	* This was addressed by extracting the ad length data and year aired data then plotting it on MatPlotLib scatter plots. Linear regressions were ran on the data to develop a predictive model. An outlier analysis was performed to rule out any potential outliers. The same linear regression was ran to observe the effects after outliers were removed.

## Hypothesis Test
Our hypothesis was that YouTube videos with the 'Funny' tag received more views than videos without the 'Funny' tag. The null hypothesis was that there is no statistically significant difference in view counts when randomly sampled between the 'Funny' and 'Not Funny' videos. The results are discussed in the Final Data Analysis Jupyter Notebook.

## Further Examination
A valuable insight into the success of each ad campaign would be to extract the monetary gain for each company after the airing of their ads.