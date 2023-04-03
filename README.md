# Business Analysis Simulation

## Background 
---
Vivendo is a fast food chain in Brazil with over 200 outlets.
Customers often claim compensation from the company for food poisoning.
The legal team processes these claims. The legal team has offices in four locations.
The legal team wants to improve how long it takes to reply to customers and close claims.
The head of the legal department wants a report on how each location differs in the time it
takes to close claims.

## Overview
---

### **This Report gives a Visualization and Analysis of Four Legal Teams in Charge of Claims from the Brazilian Fast Food Chain Vivendo, I would like to Solve these Tasks Carefully :**

Is their Data Correct to their own Analysis of each Description?
Create Visualizations of the Number of Claims to Each Location, Distribution of Time to close for all claims, and the Relationship between Time to Close and Location

## The Data 
### Let's Take Quick Look at the Columns
Before Going in and Attempting to tweak and edit the Data let's look at if it coalines with what the Company understands so far.
After checking each piece of Data I compiled a checklist of whether or not they got their own analysis right.

![Checks](https://user-images.githubusercontent.com/129571496/229391523-90eaeae0-2faa-43ba-a588-186e1dfcad76.PNG)

### This is the Full Diagnosis to check the Data Set for Matching the Description
![Columns](https://user-images.githubusercontent.com/129571496/229391705-3df19c76-9667-4cc3-9cc1-e8c8e52ca754.PNG)

After Looking at our Data, we can see there are some missing values. I am going to Filter which Columns I will use, and round columns claim_amount and amount_paid so we can make the Description Accurate. Additionally, I will make it so both claim_amount and amount_paid are concurrently updated by utilizing a repeating if else function until we reach a null to have Continuous Updates of Information
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
