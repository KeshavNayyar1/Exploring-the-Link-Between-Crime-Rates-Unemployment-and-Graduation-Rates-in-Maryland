# Exploring-the-Link-Between-Crime-Rates-Unemployment-and-Graduation-Rates-in-Maryland2
Introduction: Exploring the Relationship Between Crime, Unemployment, and Education
The relationship between socioeconomic factors and educational outcomes has long been a subject of interest in social science research. Specifically, crime rates, unemployment levels, and education (graduation rates) are often interrelated, with each factor influencing the other in complex ways. For example, counties with higher crime rates may experience disruptions in education, while areas with higher unemployment rates may see lower graduation rates as economic hardship affects student performance and school attendance. Conversely, higher education levels can contribute to lower unemployment and crime rates by providing individuals with more opportunities.

In this analysis, we investigate the linkages between graduation rates, unemployment rates, and crime rates across various counties in Maryland. By using statistical tests such as Z-tests, T-tests, Chi-squared tests, ANOVA, and OLS regression, we examine how these factors are related to each other.

Overview of the Datasets
Graduation Rate Data: This dataset provides the graduation rates for Maryland counties. The graduation rate represents the percentage of students who complete high school in a given year. Counties are labeled, and the graduation rates span across several years (2020 to 2023). This dataset serves as the primary indicator of educational success in different counties.

Key Variables: County, Graduation Rate (%)
Example:
java
Copy code
County        | Graduation Rate (%)
Baltimore City | 68.7
Baltimore      | 84.5
Unemployment Rate Data: The unemployment rate dataset provides the percentage of the working-age population that is unemployed in each county. The unemployment rate is presented for different years (e.g., 2020, 2021, etc.). This is used to understand how economic hardship correlates with graduation rates.

Key Variables: County, Unemployment Rate (%)
Example:
java
Copy code
County          | Unemployment Rate (2020)
Baltimore City  | 8.5
Baltimore       | 6.6
Crime Data: This dataset focuses on violent crime rates, specifically crimes such as murder, rape, robbery, and assault, across Maryland counties. Crime is measured annually and includes various categories of violent crime rates. The crime rates serve as an indicator of safety and social stability, and their potential impact on education is analyzed.

Key Variables: County, MURDER, RAPE, ROBBERY, AGG. ASSAULT, etc.
Example:
Copy code
County          | MURDER | RAPE | ROBBERY | AGG. ASSAULT
Baltimore City  |   10   |  20  |   50    |    100
Baltimore       |   5    |  10  |   25    |     80
Data Combination To explore how these factors interact, the datasets are merged based on the county names. For example, we combine graduation rates with unemployment and crime data, aligning the information by jurisdiction for each county. This combined dataset allows us to perform various statistical tests to assess the relationships between the variables.

Explanation of the Statistical Tests
Chi-Squared Test: The Chi-squared test was used to determine if there is a relationship between graduation rate categories (low, medium, high) and unemployment rate categories (low, medium, high). The test helps us understand whether the distribution of counties across these categories occurs by chance or if there is a significant association.

Z-Test: A Z-test was performed to compare the mean graduation rates and murder rates. This test determines if there is a statistically significant difference between the two means and assesses whether counties with higher murder rates tend to have lower graduation rates.

T-Test: The T-test compared the graduation rates between counties with low and high unemployment rates. By dividing the counties into two groups based on unemployment, we examined whether unemployment significantly impacts graduation rates.

ANOVA: An ANOVA (Analysis of Variance) test was conducted to compare graduation rates across different unemployment rate categories. This test checks if the differences between the graduation rates in these groups are statistically significant.

OLS Regression: We performed OLS (Ordinary Least Squares) regression to assess the relationship between murder rates and graduation rates. This test quantifies the extent to which an increase in the murder rate affects the graduation rate and provides insight into the strength of the relationship between crime and education.

These tests help us quantify the relationships between the variables and determine whether crime rates, unemployment, and graduation rates are linked in Maryland counties.

In the next section, we’ll summarize the findings from these statistical analyses and interpret their implications.
<img width="1134" alt="Screenshot 2024-09-07 at 10 50 59 PM" src="https://github.com/user-attachments/assets/32271070-8345-4a97-8cdc-4a432d416ada">
<img width="1141" alt="Screenshot 2024-09-07 at 10 53 16 PM" src="https://github.com/user-attachments/assets/86e148af-3cad-4a12-9515-0a510fd0dec8">
<img width="1139" alt="Screenshot 2024-09-07 at 10 53 23 PM" src="https://github.com/user-attachments/assets/e16fbe75-619f-4691-9cf6-47c4fcbfbeb2">

