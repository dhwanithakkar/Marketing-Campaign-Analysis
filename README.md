# Marketing Campaign Analysis

## Problem Statement

Given a dataset containing information on the Facebook and AdWords marketing campaigns. As far as clicks, conversions, and overall cost-effectiveness are concerned, we must decide which platform performs better.

Primary objective is to maximize the return on investment (ROI) for XYZ company.

## Dataset

The dataset compares performance of 2 seperate Ad campaigns conducted throughout 2019. Each ad campaign's performance indicators are included in the dataset, which offers insights into the campaigns' effectiveness and efficiency over time.
A total of 365 rows are present, one for each day.

It contains the following columns:

Date,
Ad Views,
Ad Clicks, Ad Conversions, Cost per Ad, Click through Rate (CTR), Conversion Rate, Cost per Click (CPC).

Below is a snapshot of the dataset for better understanding.

![Screenshot 2024-08-10 160159](https://github.com/user-attachments/assets/13113be5-db45-497c-ac7c-18f4058a1d8d)

### Steps followed 

Exploratory Data Analysis (EDA):
- Step 1 : Import all the necessary libraries and load the dataset into Jupyter Nootbook, dataset is a csv file.
- Step 2 : Using the decribe() function, descriptive statistics were verified. This gives us insight into the mode, mean, median, and other concepts.

Comparing Campaigns performance:
- Step 3 : Histograms made for analyzing distribution of the clicks and conversions for Facebook and AdWords.
- Step 4 : Finding out how frequently do we observe days with high numbers of conversions compared to days with low numbers of conversions. 
  Creating a function to calculate the category for the conversions. Below are the categories.

      (a) Less than 6

      (b) 6-10

      (c) 10-15

      (d) More than 15
 ![a](https://github.com/user-attachments/assets/47e1be1b-3e2a-419e-bf88-c39316138cd2)

   This suggests Facebook had more frequent higher conversion days than AdWords, which either had very low conversion rates (less than 6) or moderate ones (6 - 10).

- Step 5 :  Also calculating correlation coefficient to check do more clicks on an Ad lead to more sales?

![c](https://github.com/user-attachments/assets/4056def3-685a-4dd9-ae3a-6873e4d017a9)

A correlation coefficient of 0.87 indicates a strong positive linear relationship between clicks on Facebook ads and sales. This suggests that as the number of clicks on Facebook ads increases, sales tend to increase as well.
This strong correlation suggests that Facebook ads are highly effective in driving sales.

A correlation coefficient of 0.45 indicates a moderate positive linear relationship between clicks on AdWords ads and sales. While there is still a positive relationship, it is not as strong as with Facebook ads.


HYPOTHESIS TESTING:

 Hypothesis: Advertising on Facebook will result in a greater number of conversions compared to advertising on AdWords. 

Null Hypothesis (H0): There is no difference in the number of conversions between Facebook and AdWords, or the number of conversions from AdWords is greater than or equal to those from Facebook.

Alternate Hypothesis (H1): The number of conversions from Facebook is greater than the number of conversions from AdWords.

- Step 6 :  Finding out mean conversion for both Ad campaings.

![d](https://github.com/user-attachments/assets/44f4c864-3184-440e-a007-cb3389b7bd42)

The mean number of conversions from Facebook ads (11.74) is substantially higher than the mean number of conversions from AdWords ads (5.98). This suggests that, on average, Facebook advertising is more effective in generating conversions compared to AdWords advertising.

- Step 7 : Conducting ttest_ind test -> This is a test for the Null Hypothesis that two independent variables have identical average values.
![e](https://github.com/user-attachments/assets/bb50b4f9-195f-4912-8a74-7035eaa85ce8)

The T statistic (32.88) is a measure of the difference between the means of the two groups relative to the variation within the groups. A larger T statistic indicates a greater difference between the means of the two groups.

The p-value (9.35e-134) is extremely small, indicating strong evidence against the null hypothesis.
The results strongly support the alternate hypothesis, indicating that the number of conversions from Facebook advertising is indeed greater than the number of conversions from AdWords advertising. 

RESULT: Facebook advertising appears to be a more effective channel for generating conversions compared to AdWords advertising, based on the sample data analyzed.

REGRESSION ANALYSIS:

What will happen when I do go with the Facebook Ad? How many facebook ad conversions can I expect given a certain number of facebook ad clicks?

Our independent variable - Facebook Ad Clicks and Dependent variable - Facebok Ad Conversions
- Step 8 : Initializing linear regression model. When we perform prediction for a continuous variable then, evaluation metrics used is 'mean_squared_error' and 'R square score'.
  
![f](https://github.com/user-attachments/assets/4e10a739-bd6f-4f3e-bc89-fae0170c3b30)

- Step 9 : Plotting a scatter plot and finding out the best fit line.
![g](https://github.com/user-attachments/assets/deca9c31-623b-4ea6-b7a3-22391090463f)
![h](https://github.com/user-attachments/assets/6ae71015-a12e-475c-bad7-b59525e88972)


TIME SERIES ANALYSIS:
- Step 10 : Analyzing Facebook campaign metrics over time.

     At what times of the month or days of the week do we observe the conversions?

- Step 11: Extracting month and weekday from date column ans plotting a bar chart for Weekly conversions and a line chart for monthly conversions.
  
![i](https://github.com/user-attachments/assets/9c9387c1-f302-4932-953c-15a0f3a3cf91)
![j](https://github.com/user-attachments/assets/8e34fe8b-d304-473a-a614-95cdc80313b7)

WEEKLY - The total number of conversions remains relatively consistent, indicating a consistent level of engagement throughout the week. However, Mondays and Tuesdays consistently exhibit the highest conversion rates compared to other days.

MONTHLY - A general increase in conversions over time. However, certain months stand out with variations in conversion rates. February, April, May, June, August, and November experience a decline in conversions compared to neighboring months.





