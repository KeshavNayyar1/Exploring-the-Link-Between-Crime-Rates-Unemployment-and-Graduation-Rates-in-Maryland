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
<img width="1179" alt="Screenshot 2024-09-07 at 11 01 16 PM" src="https://github.com/user-attachments/assets/f24978ad-411b-4209-81cf-b8afa5e31b74">

<img width="1214" alt="Screenshot 2024-09-07 at 11 04 43 PM" src="https://github.com/user-attachments/assets/3e2af290-9b3e-4123-a01f-6a4169c30365">
<img width="1138" alt="Screenshot<img width="1143" alt="Screenshot 2024-09-07 at 11 02 17 PM" src="https://github.com/user-attachments/assets/ec342021-77a4-454c-9fb5-8f92c0cfd362">


<img width="317" alt="Screenshot 2024-09-07 at 11 05 24 PM" src="https://github.com/user-attachments/assets/d56cc515-a289-4681-9f83-6407b0efa61c">


<img width="1133" alt="Screenshot 2024-09-07 at 11 14 17 PM" src="https://github.com/user-attachments/assets/9a98bfc7-10d7-4927-acd3-d405c9bc842e">


<img width="829" alt="Screenshot 2024-09-07 at 11 06 09 PM" src="https://github.com/user-attachments/assets/383a8191-8bb0-49fa-973a-ea1a5bfc443c">

<img width="658" alt="Screenshot 2024-09-07 at 11 15 51 PM" src="https://github.com/user-attachments/assets/b6f187a7-cea1-4cc7-9946-1becee54b550">
<img width="757" alt="Screenshot 2024-09-07 at 11 16 26 PM" src="https://github.com/user-attachments/assets/9d617941-4d79-4d22-ad90-f38e90641aae">
<img width="740" alt="Screenshot 2024-09-07 at 11 16 59 PM" src="https://github.com/user-attachments/assets/0380e579-d47c-49be-9196-ac8ff0d51b55">


The OLS Regression Results provide insights into how the murder rate affects the graduation rate. Here's a breakdown of the key information:

1. R-squared: 0.569
R-squared is a measure of how well the independent variable (murder rate) explains the variation in the dependent variable (graduation rate).
An R-squared of 0.569 means that 56.9% of the variation in graduation rates can be explained by changes in the murder rate. This is a moderate level of explanatory power, suggesting that the murder rate has a meaningful influence on the graduation rate, but other factors also contribute to the variation.
2. Coefficient for MURDER: -0.0706
This coefficient tells you how much the graduation rate changes for each unit increase in the murder rate.
The coefficient is -0.0706, meaning that for every 1-unit increase in the murder rate, the graduation rate is expected to decrease by 0.0706%. This suggests a negative relationship between the murder rate and the graduation rate—when the murder rate goes up, the graduation rate tends to go down.
3. P-value for MURDER: 0.000
The p-value for the murder rate coefficient is 0.000, which is far below the common significance level of 0.05.
This means the negative relationship between the murder rate and graduation rate is statistically significant. You can confidently say that the murder rate has a real effect on the graduation rate.
4. F-statistic: 26.37, Prob (F-statistic): 5.04e-05
The F-statistic evaluates the overall significance of the regression model. A value of 26.37 and a very small p-value (5.04e-05) indicate that the model as a whole is statistically significant, meaning the murder rate significantly affects graduation rates.
5. Intercept (const): 90.5611
The intercept represents the expected graduation rate when the murder rate is zero. In this case, the graduation rate would be about 90.56% if there were no murders.
6. Interpretation of Results
The regression results show that as the murder rate increases, the graduation rate tends to decrease. The relationship is both negative and statistically significant.
For every additional murder, the graduation rate is expected to drop slightly by 0.0706%, and the model explains a moderate amount of the variation in graduation rates across the counties.
7. Conclusion
The results strongly suggest that higher murder rates are associated with lower graduation rates in the counties analyzed. Given the significance of the results, policymakers could consider the potential impacts of violent crime on educational outcomes in their decision-making.


<img width="555" alt="Screenshot 2024-09-07 at 11 18 57 PM" src="https://github.com/user-attachments/assets/f8268e5d-ebef-4b89-b730-03f2bc8fe5ca">

<img width="874" alt="Screenshot 2024-09-07 at 11 19 24 PM" src="https://github.com/user-attachments/assets/fc4d0387-94b5-44e9-96fd-bbc2bc6cb245">
