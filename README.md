# Probject Overview

In this case study, I analyzed Yulu’s shared electric cycle rental data to understand the key factors influencing demand. Yulu, India’s leading micro-mobility service provider, needed to identify what drives usage patterns to make strategic operational and marketing decisions.

#  Business Problem
Yulu wants to understand which variables significantly affect the demand for shared electric cycles in India. By identifying these factors, Yulu can better plan station placements, adjust fleet availability, and design targeted marketing strategies.

# Approach & Analysis
Data Exploration & Cleaning:

Explored data structure, checked types, converted categorical columns, and handled missing values.

Performed univariate analysis to understand distributions (e.g., temperature, humidity, windspeed, count).

Visualized categorical attributes such as season, weather, holiday, and working day.

Bivariate Analysis:

Examined relationships between demand (count) and season, weather, working day, etc.

Used boxplots, violin plots, and scatter plots to identify patterns.

Hypothesis Testing:

Working Day Impact: Used two-sample t-test to analyze if cycle demand differs between working and non-working days.

Result: p-value = 0.0199. Significant difference found. Interpretation: Demand varies due to commuting patterns.

Seasonal Effect: Conducted ANOVA to test if mean demand differs across seasons.

Result: p-value < 1e-125. Very strong seasonal influence.

Weather Effect: Conducted ANOVA to check demand differences by weather conditions.

Result: p-value ≈ 1.84e-37. Poor weather reduces demand significantly.

Season vs Weather Dependency: Used Chi-square test to check association between season and weather.

Result: p-value = 3.64e-07. Strong dependency — certain weather patterns dominate specific seasons.

Normality & Assumptions:

Checked distribution of rental counts (right-skewed, leptokurtic).

Applied Box-Cox transformation to approximate normality for robust testing.

Verified assumptions using Q-Q plots and Shapiro-Wilk tests.


#  Key Insights

Demand is Skewed: Cycle rental counts are not normally distributed; most days see lower demand with a few high-demand days.

Seasonal Dependence: Season is a strong driver of demand; demand is higher in certain seasons (likely spring/fall) and drops during extreme weather.

Weather Sensitivity: Bad weather (e.g., rain, thunderstorms) reduces rentals significantly.

Working Day Patterns: Commuting behavior affects usage; non-working days show slightly different patterns, suggesting leisure trips dominate on weekends/holidays.

Season & Weather Link: High dependency implies that season and weather should be carefully modeled to avoid multicollinearity.
