GDP vs Press Freedom Analysis (EU Countries)

Project Overview

My project builds on existing research that examines the relationship between the World Press Freedom Index and broader indicators of economic and political development. Although the press freedom index is widely used, its credibility has been questioned, making it important to compare it with other measures such as GDP per capita, the democracy index, and the global freedom index.
Previous studies have found that countries with higher levels of economic prosperity, democratic governance, and civil freedoms tend to score higher on press freedom. In particular, regression analyses show positive relationships between press freedom and these indicators, while grouped comparisons reveal that countries with stronger economic and democratic conditions consistently exhibit higher press freedom levels.
Building on these findings, this project further explores these relationships, comparing two datasets: "GDP per country" and "Press Freedom score". By replicating and extending this type of analysis, the project aims to better understand how press freedom is associated with key global development indicators and to evaluate whether similar patterns can be observed in the data used here.
For my project, I decided to analyse only the countries in the European Union. Due to the fact that the "GDP per Country" dataset examines data from 2020-2025, while the "Press Freedom Score" from 1979 until 2025, I made the decision to limit my research only to 2023. I deliberately chose this year because the previous three years, 2020, 2021, and 2022 (which are common to both datasets), were highly affected by the COVID-19 pandemic, and I expect that the results wouldn't be representative enough for all the EU countries. 
The results of my first analysis were contrary to what I expected to find, which is the reason why I decided to conduct a case study with one specific country for a period of three years. In it, I  compared both the GDP and the Press Freedom score for a period of 3 years. The aim is to observe whether there is a connection between the two indicators for a longer time period in an isolated case(not being compared with other bigger, smaller, richer, or poorer countries). For this analysis, I chose Bulgaria due to my own proximity to the country. 


The main objective is to determine whether countries with higher GDP tend to have higher levels of press freedom.

 Datasets

1. GDP Dataset
	•	Contains GDP values for multiple countries
	•	Originally in wide format (years as columns)
	•	Transformed into long format using pandas.melt()

2. World Press Freedom Dataset
	•	Contains press freedom scores by country and year
	•	Includes:
	•	Country
	•	Year
	•	Score

⸻

Data Processing

The following steps were performed:
	•	Converted GDP data from wide to long format
	•	Filtered data for the years 2020–2023
	•	Selected only EU countries
	•	Standardized country names (e.g., “Czech Republic” → “Czechia”)
	•	Removed missing values
	•	Converted data types for consistency
	•	Merged datasets using:
	•	Country
	•	Year

⸻

 Final Dataset

The final dataset contains the following columns:
	•	Country
	•	Year
	•	GDP_value
	•	Press Freedom Score

⸻

 Analysis

1. Scatter Plot

A scatter plot was used to visualize the relationship between GDP and press freedom.
Each point represents a country-year observation.

2. Log-Log Plot

A log-log transformation was applied to better visualize differences in GDP across countries.

3. Country-Specific Analysis (Bulgaria)

A separate analysis was performed for Bulgaria:
	•	GDP and press freedom were plotted over time (2020–2023)
	•	A dual-axis line chart was used for better comparison

⸻

 Correlation Analysis
	•	EU Countries:
Correlation ≈ 0.12 → very weak relationship
	•	Bulgaria:
Calculated separately (limited observations)

⸻

Key Insights
	•	The relationship between GDP and press freedom is weak
	•	Economic performance alone does not strongly determine media freedom
	•	Other political and social factors likely play a significant role
	•	Log-scale visualization improves interpretability

⸻

Technologies Used
	•	Python 
	•	pandas
	•	matplotlib
	•	seaborn
	•	Jupyter Notebook


Future Improvements
	•	Include more years of data
	•	Analyze additional countries
	•	Use GDP per capita instead of total GDP
	•	Apply regression models
