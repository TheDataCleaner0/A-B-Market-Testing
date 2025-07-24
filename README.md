# A/B-Market-Testing
This repository contains a data analysis project focused on an A/B test conducted by a marketing company to evaluate the effectiveness of an advertising campaign (ad group) compared to a Public Service Announcement (psa group) in driving user conversions.

## Project Goals
The primary objectives of this project were to answer the following questions:
* Campaign Success: Determine if the advertising campaign (ads) was statistically successful in increasing user conversion rates.
* Attribution of Success: Quantify the potential financial impact and success attributed to the ad campaign.
* Marketing Insights: Provide actionable insights to optimize future marketing strategies based on campaign performance across different days and hours.

## Dataset (/kaggle/marketing-ab-testing/marketing_AB.csv)
* user id: Unique identifier for each user.
* test group: Indicates whether the user was exposed to the 'ad' (experimental group) or 'psa' (control group).
* converted: A boolean (True/False) indicating whether the user converted.
* total ads: The total number of ads seen by the user.
* most ads day: The day of the week when the user saw the most ads.
* most ads hour: The hour of the day when the user saw the most ads.

## Methodology
The project followed a standard A/B testing methodology:
* Data Understanding: Loaded and performed initial cleaning and exploratory data analysis on the marketing_AB.csv dataset. This included checking for missing values, data types, and basic descriptive statistics, noting the imbalance in group sizes.
* Hypothesis Definition:
Null Hypothesis (H_0): The conversion rate of users exposed to ads is less than or equal to the conversion rate of users exposed to PSAs (P_ad <= P_psa). Alternative Hypothesis (H_1): The conversion rate of users exposed to ads is greater than the conversion rate of users exposed to PSAs (P_ad> P_psa).
* Hypothesis Testing: A Z-test for proportions was conducted to determine if the observed difference in conversion rates between the 'ad' and 'psa' groups was statistically significant, using a one-tailed test.
* Intermediate Analysis & Visualization: Explored conversion rates based on most ads day, most ads hour, and custom time_interval categories (Morning, Afternoon, Evening, Night) to identify temporal patterns and potential optimization opportunities.
* Conclusion & Recommendations: Summarized the statistical findings and provided actionable recommendations for the marketing team

## Key Findings
* Statistical Significance: The A/B test concluded that the 'ad' campaign significantly outperformed the 'psa' in terms of conversion rates. The Null Hypothesis was rejected, indicating that the higher conversion rate for the 'ad' group was not due to random chance.

* Conversion Rates:'ad' group conversion rate: ~3.19%, 'psa' group conversion rate: ~2.53%. This represents an approximate 0.66 percentage point increase in conversion rate attributable to the ads.

