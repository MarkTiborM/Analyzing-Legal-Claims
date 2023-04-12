# Business Analysis Simulation

## Background Information Provided
---
Vivendo is a fast food chain in Brazil with over 200 outlets.
Customers often claim compensation from the company for food poisoning.
The legal team processes these claims. The legal team has offices in four locations.
The legal team wants to improve how long it takes to reply to customers and close claims.
The head of the legal department wants a report on how each location differs in the time it
takes to close claims.

## Overview
---

### **This Report gives a Visualization and Analysis of Four Legal Teams in Charge of Claims from the Brazilian Fast Food Chain Vivendo, they would like me to do the following:**

1.) Create a checklist of null/uninterpretable data to give their dataframe a thorough analysis

2.) Create Visualizations of the Number of Claims to Each Location, Distribution of Time to close for all claims, and the Relationship between Time to Close and Location

3.) Create a concrete Conclusion of the analysis to give potential investigative opportunities to the company to see if their is a correlation between the locations

DATA VALIDATION :
Data Checks :
1.) claim_id:
The values are integers, matching the description provided.There are 2000 non-null values, indicating that there are no missing values in this column.

2.) time_to_close:
The values are integers, matching the description provided. There are 2000 non-null values, indicating that there are no missing values in this column.

3.) claim_amount:
The values are objects, matching the descritpion as Brazilian currency, beginning with R$.There are 2000 non-null values, indicating that there are no missing values in this column.

4.) amount_paid:
The values are floats, matching the description provided. There are 1964 non-null values, indicating that there are 36 missing values in this column. To address the missing values, I replaced the missing values with the overall median amount paid as specified in the requirements.

5.) location:
The values are objects, matching the description provided. There are 2000 non-null values, indicating that there are no missing values in this column.

6.) individuals_on_claim:
The values are integers, matching the description provided. There are 2000 non-null values, indicating that there are no missing values in this column.

7.) linked_cases:
The values are objects, matching the description provided. There are 1974 non-null values, indicating that there are 26 missing values in this column. I replaced the missing bools with FALSE as specified in the requirements.

8.) cause:
The values are objects, matching the description provided. There are 2000 non-null values, indicating that there are no missing values in this column.

Data Description :
The original data is 2000 rows and 8 columns. The first thing I did was remove the missing values for location, replaced the missing values with zero for individuals_on_claim, replaced missing values with FALSE for linked_cases, and then replaced missing values with 'unknown' for cause. To ensure we have an accurate description of the columns, I finally replaced the missing values with the overall median amount paid for amount_paid.

After cleaning and processing the data, here are some key findings:
There are 0 duplicated rows as expected. For the amount_paid column, there are only 1964 observations, indicating 36 missing values. The range of values goes from 1516.72 to 52498.75 Brazilian Real (BRL). The mean amount paid is 21541.975183 BRL, with a standard deviation of 12530.156509 BRL. For the individuals_on_claim column, there are 2000 observations, and the range of values goes from 1 to 15. The mean number of individuals on each claim is 8.0495, with a standard deviation of 4.087347. For the claim_id column, there are 2000 observations, and the range of values goes from 1 to 2000. For the time_to_close column, there are also 2000 observations, and the range of values goes from 76 to 518. The mean (average) time to close is 185.568 days, with a standard deviation of 49.163 days.

Wrap Up
--
After performing Exploritary Data Analysis drafting (creating histograms) I can assume that the data has little to no limitations for creating the plots after cleaning and validation.



# read in the data as a pandas dataframe
import pandas as pd

df = pd.read_csv("your_file.csv")

# this code checks for missing values in each column

    for col in df.columns:

    num_missing = df[col].isnull().sum()
    
    if num_missing > 0:
    
        print(f"{col} has {num_missing} missing values.")
        
    else:
    
        print(f"{col} has no missing values.")
        
![Checks](https://user-images.githubusercontent.com/129571496/229391523-90eaeae0-2faa-43ba-a588-186e1dfcad76.PNG)
### This is the Full Diagnosis to check the Data Set for Matching the Description
![Columns](https://user-images.githubusercontent.com/129571496/229391705-3df19c76-9667-4cc3-9cc1-e8c8e52ca754.PNG)

After Looking at our Data, we can see there are some missing values. I am going to filter which columns I will use, and round columns claim_amount and amount_paid so we can make the description Accurate. Additionally, I will make it so both claim_amount and amount_paid are concurrently updated by utilizing a repeating if else function until we reach a null to have continuous updates of information
# Visualization for Number of Claims to Each Location
---
![output-3](https://user-images.githubusercontent.com/129571496/229392014-eb3a6a7f-c080-4452-9c44-e675ff3575f5.jpg)

According to the provided data, the location with the highest number of claims is RECIFE, which suggests that this location might be processing more claims than other locations. Additionally, calculating the mean and median of the number of claims proves that the Data is not balanced. There is a large gap between the top two, and bottom two Legal Teams.
# Visualization for Time to Close for all Claims
---
![Describe_relationship_between_time _to_close_for_all_locations_v 2](https://user-images.githubusercontent.com/129571496/229392121-69dbf82a-7162-483b-a8db-17bacf2d5df4.jpg)

Process: First, filled in the missing values in amount_paid and replaced the missing information in linked_cases with False. Then, calculated the 'days_to_close' column and then grouped the data by location, and calculated the mean and median values for each group. Finally, generated a bar plot with 200 bins to correctly describe each claim as accurately and simple as possible.
# Visualization for Relationship between Time to Close and Location
---
![Mean Minutes to Close - Per Location](https://user-images.githubusercontent.com/129571496/229392198-1d39dde0-8b99-417f-b65e-613d0441897a.PNG)

Explanation: For this Graph I have decided to go with a Scatter plot to account for concurrently updating Data, if there is new Data the information will update with it accordingly and make it easily comparable to see any change in the data for any business changes/updates. The relationship between the time to close the claim, and the location is that SAO LUIS takes the longest time for closing a claim although they are not the Legal Team with the most claims, NATAL is the second highest, both are much larger than the other two which leads to speculation, does the reason for the long wait times have a connection between these two branches..

# Conclusion
---
I would like to recommend that you investigate the legal claims process in the SAO LUIS branch. According to our analysis of the data, SAO LUIS seems to be taking significantly longer than other branches to process legal claims. It may be worth examining the reasons for this delay and finding ways to improve the efficiency of the process. Additionally, it may be worthwhile to investigate whether there is any link between the performance of SAO LUIS and the NATAL Legal Teams.

I believe that investigating the causes of the delay in the SAO LUIS Legal Team and assessing any possible link between the two branches will help to improve the performance of the legal department and ultimately benefit the company as a whole.
