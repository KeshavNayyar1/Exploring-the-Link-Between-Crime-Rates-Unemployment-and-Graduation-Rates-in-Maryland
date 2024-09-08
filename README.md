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
Data Combination
