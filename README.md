GDP vs Press Freedom Analysis (EU Countries)

 Project Overview

This project investigates the relationship between economic performance (GDP) and press freedom across European Union countries during the period 2020–2023.

The main objective is to determine whether countries with higher GDP tend to have higher levels of press freedom.

⸻

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
	•	Standardized country names (e.g. “Czech Republic” → “Czechia”)
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
