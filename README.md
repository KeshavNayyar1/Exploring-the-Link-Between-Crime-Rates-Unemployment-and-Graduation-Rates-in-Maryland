`# Exploring-the-Link-Between-Crime-Rates-Unemployment-and-Graduation-Rates-in-Maryland2
Introduction: Exploring the Relationship Between Crime, Unemployment, and Education
The relationship between socioeconomic factors and educational outcomes has long been a subject of interest in social science research. Specifically, crime rates, unemployment levels, and education (graduation rates) are often interrelated, with each factor influencing the other in complex ways. For example, counties with higher crime rates may experience disruptions in education, while areas with higher unemployment rates may see lower graduation rates as economic hardship affects student performance and school attendance. Conversely, higher education levels can contribute to lower unemployment and crime rates by providing individuals with more opportunities.



# Data Curation
<img width="1134" alt="Screenshot 2024-09-07 at 10 50 59 PM" src="https://github.com/user-attachments/assets/32271070-8345-4a97-8cdc-4a432d416ada">

The code imports various libraries for data analysis, statistical testing, and machine learning. It enables the user to handle data efficiently, visualize it using plots, and perform tests like T-tests and Chi-squared tests, with additional support for building neural networks if needed.

<img width="1141" alt="Screenshot 2024-09-07 at 10 53 16 PM" src="https://github.com/user-attachments/assets/86e148af-3cad-4a12-9515-0a510fd0dec8">
This code snippet is reading in four CSV files using the pandas library and storing them into four separate DataFrames:

df_county holds data about violent and property crime by county from 1975 to the present.
df_crime contains data about violent and property crime by municipality from 2000 to the present.
df_graduationrate stores data on Maryland graduation rates by county.
df_unemployment contains data on unemployment rates by county in Maryland.
<img width="1139" alt="Screenshot 2024-09-07 at 10 53 23 PM" src="https://github.com/user-attachments/assets/e16fbe75-619f-4691-9cf6-47c4fcbfbeb2">
<img width="1179" alt="Screenshot 2024-09-07 at 11 01 16 PM" src="https://github.com/user-attachments/assets/f24978ad-411b-4209-81cf-b8afa5e31b74">

This image displays the first five rows of a DataFrame (df_county), showing crime data for Allegany County from 1975 to 1979, including various columns like population, murder, rape, robbery, assault, theft, and the respective rates per 100,000 people. This is just to give a breif showing of what the dataset has. 

<img width="356" alt="Screenshot 2024-09-08 at 1 07 04 PM" src="https://github.com/user-attachments/assets/8a34794e-f7f0-4481-9965-e0ba56ccb761">

This image shows the first five rows of the df_graduationrate DataFrame, which contains the graduation rates for different counties in Maryland. The columns include County and Graduation Rate (%). This is just to give a breif showing of what the dataset has. 


<img width="392" alt="Screenshot 2024-09-08 at 1 09 37 PM" src="https://github.com/user-attachments/assets/334a7f32-bc83-4cda-88bd-56f9269b99ce">

This image shows the first five rows of the df_unemployment DataFrame, which contains unemployment rates from 2020 to 2023 for different counties in Maryland. The data includes statewide unemployment rates as well as rates for specific counties like Allegany County, Anne Arundel County, Baltimore City, and Baltimore County. The unemployment rate has been decreasing over the years across all listed regions.

# Exploratory Data Analysis

This code is all about combining data on crime rates and graduation rates for Maryland counties to see if there's any connection between the two. First, it cleans up the data (like fixing county names and turning percentages into numbers). Then it grabs the most recent crime data and picks out important columns (like murder and robbery). After merging the crime data with the graduation rates, it calculates correlations to see how these factors relate. Finally, it saves the results to a CSV file so you can easily check out the findings later.

<img width="1133" alt="Screenshot 2024-09-07 at 11 14 17 PM" src="https://github.com/user-attachments/assets/9a98bfc7-10d7-4927-acd3-d405c9bc842e">


<img width="829" alt="Screenshot 2024-09-07 at 11 06 09 PM" src="https://github.com/user-attachments/assets/383a8191-8bb0-49fa-973a-ea1a5bfc443c">

<img width="658" alt="Screenshot 2024-09-07 at 11 15 51 PM" src="https://github.com/user-attachments/assets/b6f187a7-cea1-4cc7-9946-1becee54b550">


Columns in df_county_recent: This lists all the available columns in the df_county_recent DataFrame, which includes crime-related data like MURDER, RAPE, ROBBERY, LARCENY THEFT, and their corresponding rates per 100,000 people. This data provides insights into the crime statistics for different counties.

Correlation Matrix: The second image displays a correlation matrix between graduation rates and various crime statistics. The matrix reveals how each crime category (such as murder, rape, and robbery) correlates with the graduation rate. A negative correlation (e.g., -0.754 for murder and graduation rate) suggests that as the murder rate increases, the graduation rate tends to decrease. Similarly, other crime categories also show varying degrees of correlation with graduation rates.

This analysis helps understand the potential relationship between crime rates and educational outcomes in Maryland counties.


This code runs a linear regression to analyze the relationship between the murder rate and graduation rate. The murder rate is set as the independent variable, while the graduation rate is the dependent variable. A constant is added to the model, and an ordinary least squares (OLS) regression is fitted to predict how changes in the murder rate affect graduation rates. The regression summary is printed to show the model's details, including the coefficient for the murder rate. Depending on whether the coefficient is negative or positive, the code outputs whether an increase in the murder rate is associated with a decrease or increase in graduation rates. If there's no significant relationship, the code will also mention that. This helps assess how closely these two factors are connected.

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


This Python code uses matplotlib and seaborn to generate scatter plots showing the relationship between graduation rates and different crime categories. It first merges two DataFrames (df_graduationrate and df_county_recent) on a common column (County and JURISDICTION). The code then iterates over a list of crime categories like murder, robbery, and assault, and for each category, it creates a scatter plot with the graduation rate on the x-axis and the specific crime rate on the y-axis. The graph size is kept small for better display in-line, with transparency and smaller point sizes to improve clarity. The plot grid and layout are automatically adjusted to improve readability.

<img width="1139" alt="Screenshot 2024-09-08 at 12 17 45 PM" src="https://github.com/user-attachments/assets/722c467e-4606-4ede-943c-077d825d4799">


<img width="476" alt="Screenshot 2024-09-08 at 12 17 18 PM" src="https://github.com/user-attachments/assets/3537ba6e-8b65-4bc7-9d21-2ebf4d881a70">

<img width="480" alt="Screenshot 2024-09-08 at 12 18 50 PM" src="https://github.com/user-attachments/assets/4311d943-34de-426f-ab96-15aa5fabea19">

<img width="430" alt="Screenshot 2024-09-08 at 12 19 17 PM" src="https://github.com/user-attachments/assets/ed52d2fb-a5aa-4147-9702-8aac84074f70">

<img width="441" alt="Screenshot 2024-09-08 at 12 20 09 PM" src="https://github.com/user-attachments/assets/6d948f6c-7180-4dd8-b297-882690c1a106">

Graduation Rate vs. MURDER Rate: This graph shows that counties with lower graduation rates tend to have higher murder rates. As the graduation rate increases, the murder rate generally decreases, with most of the higher murder rates clustering around graduation rates below 85%.

Graduation Rate vs. ROBBERY Rate: Similar to the murder rate graph, counties with lower graduation rates seem to experience higher robbery rates. Counties with higher graduation rates (above 85%) tend to have much lower robbery rates.

Graduation Rate vs. RAPE Rate: This plot indicates a similar pattern, where lower graduation rates correspond with higher rape rates. Counties with higher graduation rates tend to see fewer instances of rape, though there are some outliers in the middle range.

Graduation Rate vs. AGG. ASSAULT Rate: The graph suggests that counties with lower graduation rates experience significantly higher aggravated assault rates. Higher graduation rates correspond with a dramatic drop in aggravated assault rates.

Graduation Rate vs. B & E Rate: The plot shows how graduation rates (x-axis) compare to the rates of breaking and entering crimes (y-axis). It appears that counties with lower graduation rates tend to have higher B & E rates, with the majority of lower crime rates observed in counties with graduation rates above 85%.

Graduation Rate vs. Larceny Theft Rate: This scatter plot depicts the relationship between graduation rates and larceny theft rates. There is a similar pattern here where counties with lower graduation rates seem to have higher theft rates, while higher graduation rate counties experience fewer larceny incidents.

Graduation Rate vs. Motor Vehicle Theft Rate: This graph shows how motor vehicle theft rates relate to graduation rates. Again, counties with lower graduation rates appear to have higher M/V theft rates, while counties with higher graduation rates tend to have lower incidents of vehicle theft.


This code is responsible for merging two datasets: one containing graduation rates and another containing unemployment rates for various counties. Here's what each part does:

Cleaning County Names:

Both df_graduationrate['County'] and df_unemployment['County'] have their "County" suffix removed and any extra spaces stripped, to ensure consistent naming conventions. This is important for the merge operation to work properly, as inconsistent names would cause mismatches.
Merging the Datasets:

The two datasets (df_graduationrate and df_unemployment) are merged on the common column 'County', using an inner join. This means only counties that are present in both datasets will be included in the final result. The merged DataFrame is stored in df_merged.
Displaying the Result:

Finally, print(df_merged) displays the resulting DataFrame after merging, allowing you to see the combined data of graduation and unemployment rates for each county.
This process helps in aligning the two datasets for further analysis.

<img width="1132" alt="Screenshot 2024-09-08 at 12 21 07 PM" src="https://github.com/user-attachments/assets/86b2124c-d388-4a9a-aa8f-2b05ac4687a2">

<img width="523" alt="Screenshot 2024-09-08 at 12 21 25 PM" src="https://github.com/user-attachments/assets/687dffb5-f604-49b9-9c1f-c1bf6a9daab6">

This table displays a combination of graduation rates and unemployment rates for various counties in Maryland. The first column lists the counties, while the second column shows the graduation rate (as a percentage) for each county. The subsequent columns display the unemployment rates from 2020 to 2023. By combining these two datasets, you can analyze the potential relationships between the graduation rates and unemployment trends over the years for each county. For example, Baltimore City has a lower graduation rate (68.7%) and higher unemployment rates compared to counties like Montgomery, which has a higher graduation rate (90.3%) and lower unemployment rates. This combined data is useful for exploring the correlation between economic factors and educational outcomes across the region.

<img width="891" alt="Screenshot 2024-09-08 at 12 22 10 PM" src="https://github.com/user-attachments/assets/1df9d447-1c2a-4504-ab3a-7bf4a48f56ff">

<img width="1073" alt="Screenshot 2024-09-08 at 12 22 30 PM" src="https://github.com/user-attachments/assets/f000dcac-6823-4841-aefb-62c007972621">

<img width="1133" alt="Screenshot 2024-09-08 at 12 22 54 PM" src="https://github.com/user-attachments/assets/34c2c3b2-437e-46c4-922f-7e66a1d6543a">

<img width="341" alt="Screenshot 2024-09-08 at 12 23 40 PM" src="https://github.com/user-attachments/assets/cf2a6288-5756-4c0f-a309-b3f871d75c96">

1. Chi-squared Statistic: 7.624
The Chi-squared statistic is a measure of how much the observed values deviate from the expected values under the null hypothesis. A higher Chi-squared value indicates that the observed data differ significantly from the expected data if the variables were independent. In this case, a value of 7.624 suggests that there is some deviation from what is expected under independence between graduation and unemployment rates.
2. P-value: 0.022
The p-value indicates the probability of observing the data if the null hypothesis (that graduation rates and unemployment rates are independent) were true.
A p-value of 0.022 means that there is a 2.2% chance that the observed association between the graduation rate and unemployment rate happened by random chance.
Since this p-value is less than the commonly used threshold of 0.05, we reject the null hypothesis. This means there is a statistically significant relationship between graduation rates and unemployment rates.
3. Expected Frequencies
Expected frequencies tell us what the values in the contingency table would be if graduation rates and unemployment rates were independent.
The table provides expected values for each category (e.g., low graduation rate, medium unemployment rate), and these values are compared with the observed values to compute the Chi-squared statistic.
For example:
For low graduation rate and low unemployment rate, the expected frequency is around 0.739.
For low graduation rate and medium unemployment rate, the expected frequency is 0.261.
These are compared to the actual observed frequencies to determine the level of deviation, which contributes to the Chi-squared value.
Summary and Conclusion
The Chi-squared test shows a significant relationship between graduation rates and unemployment rates because the p-value (0.022) is less than 0.05.
The expected frequencies give us a picture of what the data would look like if there were no relationship, and the significant Chi-squared statistic suggests that the actual data deviate from this.
Conclusion: There is a meaningful relationship between graduation rates and unemployment rates across Maryland counties for the given data.

<img width="1124" alt="Screenshot 2024-09-08 at 12 24 16 PM" src="https://github.com/user-attachments/assets/2b154a51-b36c-4749-92cf-96bd3d6348a4">

<img width="905" alt="Screenshot 2024-09-08 at 12 25 12 PM" src="https://github.com/user-attachments/assets/377eae14-c576-4c02-adaf-718dea5ad143">
<img width="1096" alt="Screenshot 2024-09-08 at 12 25 44 PM" src="https://github.com/user-attachments/assets/fb293202-e87a-4b11-aeb4-9495a700724f">

The T-test results show that there is a statistically significant difference in graduation rates between counties with high and low unemployment rates.

The T-Statistic of 2.17 indicates that the means of the two groups (counties with high vs. low unemployment) differ in a meaningful way.
The P-value of 0.042 is less than 0.05, which means the difference is statistically significant.
As a result, we can reject the null hypothesis and conclude that counties with high and low unemployment rates have significantly different graduation rates.

<img width="1028" alt="Screenshot 2024-09-08 at 12 26 25 PM" src="https://github.com/user-attachments/assets/1201fc9d-381b-4190-876f-2992d92eebac">
<img width="969" alt="Screenshot 2024-09-08 at 12 34 03 PM" src="https://github.com/user-attachments/assets/4c815d76-80ce-4d4b-a556-cb1b8b6324fd">

F-Statistic: 4.076
The F-statistic measures the ratio of variance between the groups (i.e., the variation in graduation rates between the low, medium, and high unemployment categories) compared to the variance within the groups. A higher F-statistic indicates that there is a larger difference between the groups compared to within the groups. In this case, the F-statistic of 4.076 suggests that the differences between the graduation rates of counties in different unemployment categories are noticeable.

P-value: 0.0327
The p-value tells us whether the observed differences in graduation rates across the unemployment categories are statistically significant. In this case, the p-value is 0.0327, which is less than the common threshold of 0.05. This means that there is only a 3.27% chance that the observed differences happened by random chance, indicating that the differences are statistically significant.

Conclusion
Since the p-value is less than 0.05, we reject the null hypothesis. The null hypothesis assumes that there is no difference in graduation rates between counties with low, medium, and high unemployment rates. Rejecting it means that there is a significant difference in graduation rates between counties with different unemployment rates.

Summary:
The ANOVA test results indicate that counties with different unemployment rates have significantly different graduation rates. There is a meaningful relationship between unemployment rates and graduation rates across the counties.

<img width="1121" alt="Screenshot 2024-09-08 at 12 34 43 PM" src="https://github.com/user-attachments/assets/ede46513-9cb5-4627-b029-c784aa5b2ef8">


<img width="1020" alt="Screenshot 2024-09-08 at 12 35 05 PM" src="https://github.com/user-attachments/assets/875b4070-ab07-4894-b09b-372fa1837998">

Summary of Tests, Graphs, and Findings
Chi-Squared Test (Graduation Rate vs. Unemployment Rate)

Chi-squared Statistic: 7.624
P-value: 0.022
Conclusion: There is a significant relationship between graduation rates and unemployment rates across Maryland counties. Since the p-value is less than 0.05, we reject the null hypothesis, indicating a statistical association between these variables. Counties with different unemployment rates show differences in graduation rates.
Z-Test (Graduation Rate vs. Murder Rate)

Z-Statistic: 4.192
P-value: 2.76e-05
Conclusion: There is a significant difference between graduation rates and murder rates. The test shows a strong relationship between these variables, and we reject the null hypothesis, indicating that murder rates could potentially influence graduation rates.
T-Test (Graduation Rate in High vs. Low Unemployment Counties)

T-Statistic: 2.166
P-value: 0.0419
Conclusion: There is a significant difference in graduation rates between counties with high and low unemployment rates. The test suggests that unemployment plays a role in determining graduation rates, as counties with lower unemployment have higher graduation rates.
ANOVA (Graduation Rates Across Different Unemployment Categories)

F-Statistic: 4.076
P-value: 0.0327
Conclusion: There is a significant difference in graduation rates between counties in different unemployment categories. This reinforces the findings from the T-Test, further confirming that unemployment rates impact graduation rates across multiple groups.
OLS Regression (Murder Rate vs. Graduation Rate)

R-squared: 0.569
P-value (Murder rate): 5.04e-05
Conclusion: The regression analysis shows that for every 1-unit increase in the murder rate, the graduation rate decreases by approximately 0.071%. This is a statistically significant result, suggesting that higher murder rates are strongly associated with lower graduation rates across counties.
Correlation Matrix (Graduation Rate vs. Crime Categories)

Correlation coefficients show negative relationships between graduation rates and multiple crime categories (e.g., murder, robbery, assault). This indicates that higher crime rates in a county tend to coincide with lower graduation rates.
Contingency Table and Chi-Squared Test (Graduation Rate Categories vs. Unemployment Rate Categories)

The contingency table showed expected values for counties distributed across graduation and unemployment rate categories.
Chi-squared Statistic: 5.515
P-value: 0.063
Conclusion: This analysis suggests a weak association between graduation rate categories (low, medium, high) and unemployment rate categories (low, medium, high). While the p-value is slightly above 0.05, it indicates some connection but may not be conclusive enough to reject the null hypothesis.
Key Learnings:
Murder rates and crime rates negatively impact graduation rates, suggesting that counties with higher violent crime levels tend to have lower graduation rates.
Unemployment rates are also strongly associated with graduation rates, and counties with lower unemployment tend to have higher graduation rates.
Regression and correlation analyses further support these relationships, indicating statistically significant findings across the board.
Chi-squared tests demonstrated that there are connections between graduation rates and unemployment, though the strength of these associations varies depending on how the data is categorized.
These analyses highlight the multifaceted relationships between crime, unemployment, and education, emphasizing how social factors influence graduation outcomes in Maryland counties.
