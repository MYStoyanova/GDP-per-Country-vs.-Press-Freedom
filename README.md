GDP vs Press Freedom Analysis (EU Countries)

1. Project Overview

My project builds on existing research that examines the relationship between the World Press Freedom Index and broader indicators of economic and political development. Although the press freedom index is widely used, its credibility has been questioned, making it important to compare it with other measures such as GDP per country, the democracy index, and the global freedom index.
Previous studies have found that countries with higher levels of economic prosperity, democratic governance, and civil freedoms tend to score higher on press freedom. In particular, regression analyses show positive relationships between press freedom and these indicators, while grouped comparisons reveal that countries with stronger economic and democratic conditions consistently exhibit higher press freedom levels.
Building on these findings, this project further explores these relationships, comparing two datasets: "GDP per country" and "Press Freedom score". By replicating and extending this type of analysis, the project aims to better understand how press freedom is associated with key global development indicators and to evaluate whether similar patterns can be observed in the data used here.
For my project, I decided to analyse only the countries in the European Union. Due to the fact that the "GDP per Country" dataset examines data from 2020-2025, while the "Press Freedom Score" from 1979 until 2025, I made the decision to limit my research only to 2023. I deliberately chose this year because the previous three years, 2020, 2021, and 2022 (which are common to both datasets), were highly affected by the COVID-19 pandemic, and I expect that the results wouldn't be representative enough for all the EU countries. 
The results of my first analysis were contrary to what I expected to find, which is the reason why I decided to conduct a case study with one specific country for a period of three years. In it, I  compared both the GDP and the Press Freedom score for a period of 3 years. The aim is to observe whether there is a connection between the two indicators for a longer time period in an isolated case(not being compared with other bigger, smaller, richer, or poorer countries). For this analysis, I chose Bulgaria due to my own proximity to the country. 


The main objective is to determine whether countries with higher GDP tend to have higher levels of press freedom.

 I used the following two datasets:

1. GDP Dataset

-  Contains GDP values for multiple countries
-  Originally "Years" formatted as columns
-  Pivoted into rows using pandas.melt()

2. World Press Freedom Dataset
   
- Contains press freedom scores by country and year
- Includes:
	- Country
	- Year
	- Score

3.Data Processing:

The following steps were performed:

- Converted GDP data in the right format
- Filtered data for the year 2023 and the years 2020–2023 (for my "Bulgaria" case study)
- Selected only EU countries
- Standardized country names (e.g., “Czech Republic” → “Czechia”)
- Removed missing values
- Converted data types for consistency
- Merged datasets using:
	- Country
	- Year

4. Final Dataset:

The final dataset contains the following columns:
- Country
- Year
- GDP_value
- Press Freedom Score

5. Analysis:

5.1. Combined Bar and Line plot

- A combined bar and line chart was used to visualize the relationship between GDP and press freedom across countries in 2023.
The bar chart represents GDP values for each country, while a line plot overlaid on a secondary axis shows the corresponding press freedom scores. This dual-axis approach allows for a direct comparison between economic performance and press freedom within the same visualization.
Each country is represented along the x-axis, with GDP displayed on the left y-axis and press freedom scores on the right y-axis. This method makes it easier to observe patterns and compare how press freedom varies alongside GDP across different countries.

6. Country-Specific Analysis (Bulgaria)

A separate analysis was performed for Bulgaria:
- GDP and press freedom were plotted over time (2020–2023)
- A dual-axis line chart was used for better comparison

Note* The graphic showed very interesting results for Bulgaria. A sharp decline in Press Freedom for 2022, while the GDP grows steadily. This highlights the need for more in-depth qualitative analysis to understand what other indicators played such a key role in the Press Score results. 


 7. Correlation Analysis:

 For the correlation analysis, the integrated Python Pearson Correlation Coefficient was used. This method is suitable for this scenario as it measures a linear relationship between GDP and Press Freedom score. The Pearson Correlation Coefficient is calculated using the following formula:

$$
    r = \frac{\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}
{\sqrt{\sum_{i=1}^{n}(x_i - \bar{x})^2} \cdot \sqrt{\sum_{i=1}^{n}(y_i - \bar{y})^2}}
$$

Where the used terms are:

-  $x_i$ — Press Freedom score for observation $i$
-  $y_i$ — GDP value for observation $i$
-  $\bar{x}$ — mean (average) Press Freedom score
-  $\bar{y}$ — mean (average) GDP across all observations
-  $n$ — total number of observations
-  $r$ — Pearson correlation coefficient

  The Pearson Correlation Coefficient takes values between 0 and 1, where:
 - $r > 0$ - positive linear relationship (both variables increase or decrease together)  
 - $r < 0$ - negative linear relationship (one variable increases while the other decreases)  
 - $r \approx 0$ - little or no linear relationship
   
8. Results

- EU Countries:
	
Correlation ≈ 0.12 -> very weak relationship

- Bulgaria:
	
Correlation ≈  -0.47 -> very, very weak relationship.
- N.B. Due to the limited amount of data, the correlation is not reliable for drawing conclusions.
- These results show that the relation between GDP per Country and Press Freedom is very weak. 

Key Insights:
- The relationship between GDP and press freedom is weak
- Economic performance alone does not strongly determine media freedom
- Other political, geopolitical, and social factors likely play a significant role
	
Future Improvements:

- I acknowledge the limitations I had for this research. For future improvements, it would be worth it to analyse the relationship between GDP per coutnry with the Press Freedom score for a longer period of time. Having datasets with information for 10 years would be much more representative. 
Also, expanding the analysis to non-EU countries could give interesting results. It is widely known that democracy and freedom of speech in the EU are fundamental for its existence; the overall score for press freedom is expected to be higher than in other non-EU countries. It would be interesting to observe the correlation between it and economic stability in the South American and Asian countries.

Notes:
1. For better reading of the results, I used "Cyprus" instead of "The Republic of Cyprus".


Sources: 

1. Press freedom linked to greater financial stability, finds global study, URL[https://doi.org/10.1016/j.ejpoleco.2022.102236].
2. The Role of Press Freedom in Economic Development: A Global Perspective, URL[https://www.researchgate.net/publication/235921387_The_Role_of_Press_Freedom_in_Economic_Development_A_Global_Perspective]
3. Press freedom, market information, and international trade, URL[https://doi.org/10.1016/j.ejpoleco.2022.102236]
4. Examine the Validity of the World Press Freedom Index: Analysis of the Relationship between Nominal per Capita GDP, Media Credibility, Democracy Index, and World Press Freedom Index, URL[https://www.researchgate.net/publication/390641982_Examine_the_Validity_of_the_World_Press_Freedom_Index_Analysis_of_the_Relationship_between_Nominal_per_Capita_GDP_Media_Credibility_Democracy_Index_and_World_Press_Freedom_Index]
   
