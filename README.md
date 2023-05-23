# PHASE 3 PROJECT

* # Overview
SyriaTel is a telecommunications company hoping to foresee and prevent client churn. Customer churn is the percentage of clients that quit utilizing an company's product or service during a specific time span.  This project aims to provide insights into the determining factors leading to customer  churning as well as predict future cases of churn using different models in order to provide adequate recommendations to the company. This will in turn help to retain customers / product consumers who would otherwise churn.

This helps in improve the health of the SyriaTel sevices while assisting in the forecasting of future revenue for the business. Building a classifier to predict whether a customer will ("soon") stop doing business with SyriaTel, would then provide information on patterns that may exist and shed light on the problem.SyriaTel itself who are interested in how to improve their customer rettention rates.

* # Business understanding

SyriaTel has tasked me to provide prediction analysis on whether their customers will churn anytime soon. 
The word churn means, "A measure of the number individuals or items moving out of a collective group over a specific period."That is to say Churn is a measure of how many customers stop using a product or service. It can be measured based on actual usage or failure to renew when the product is sold using a subscription mode


**Stakeholder**: SyriaTel Executives

**Business Problem**: SyriaTel is trying to predict which of their customers will churn. 


**Business Questions**: What aspects of the company's operations can they improve upon in order to retain their current customers?

* # Data Understanding

The title of this dataset is called "Churn in Telecom's dataset" from <a href="https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset">kaggle.com</a>

*Number of records: 3333
* Number of columns: 21
*Target variable: <b>churn</b>

The dataset provided information on the following features for each customers:

 ***state***, string. 2-letter code of the US state of customer residence.
***account_length***, numerical. Number of months the customer has been with the current telco provider.
***area_code***, string="area_code_AAA" where AAA = 3 digit area code.
***voice_mail_plan***, (yes/no). The customer has voice mail plan.
***number_vmail_messages***, numerical. Number of voice-mail messages.
***total_day_minutes***, numerical. Total minutes of day calls.
***total_day_calls***, numerical. Total minutes of day calls.
***total_day_charge***, numerical. Total charge of day calls.
***total_eve_minutes***, numerical. Total minutes of evening calls.
***total_eve_calls***, numerical. Total number of evening calls.
***total_eve_charge***, numerical. Total charge of evening calls.
***total_night_minutes***, numerical. Total minutes of night calls.
***total_night_calls***, numerical. Total number of night calls.
***total_night_charge***, numerical. Total charge of night calls.
***total_intl_minutes***, numerical. Total minutes of international calls.
***total_intl_calls***, numerical. Total number of international calls.
***total_intl_charge***, numerical. Total charge of international calls
***number_customer_service_calls***, numerical. Number of calls to customer service.
***churn***, (yes/no). Customer churn - target variable.


## Data Cleaning
---
To create an accurate classification model, the following steps were taken to prepare the data: 

* Checking for missing data or generic placeholders within the dataset. 
* Converting columns of the object data types, to a numerical data type.
* Dropping columns that were not pertinent to this project or not of great impact  to the business question ('phone_number', 'area_code').
* Create dummy variables for the 'state' column .

* # Modeling

For this preject I chose to use the following classification models: 

* Baseline model:Logistic regression
* Model 2: Decision tree
* Model 3: Random forest
* Model 4: K-Nearest Neighbor

I elected to use ***Recall*** as my evaluation metric for this particular project. The recall score is true positive divided by the true positive plus the false negative. It is the measure of actual observations which are predicted correctly. I chose this classification metric because we want to capture as many possible customers churning as possible, and doing so will reduce the number of false negatives(not churn). For this scenario, a false negative would be the number of identified customers as churned, but were classified as not churned. 
For this model, false negatives will cost the company more than false positives because misidentifying someone as "churned" and using customer retention strategies would be less expensive and would cost the SyriaTel more than letting a churned customer fall through the cracks. 

### Model Results

* Logistic Regression
Recall score(test) = 20%

* KNearestNeighbor
Recall score = 16%

* Decision Tree
Recall score(test) = 64%

* Random Forest
Recall score (test)= 67%

* Random Tree with Gridsearch CV
Recall score (test)= 72%

* # Recomendation

#### Recommendation 1: 

From the graph of customer service calls, I used a bar graph to depict how many customer service calls it took for a customer to make in order to increase their likelihood of churning. When a customer makes at least 4 calls to customer service, the churn rate significantly increases and this increases as the number of calls increases respectively. 

I recommend that managers come up with new training techniques to telephone attendant .This is equp them with tactics which will results into attendin to customer needsefficiently and to their full satisfatory hence reducing the number of call to be below 4 where the churn rate is low.

#### Recommendation 2: 

The next big contributor to customer churn was total day charge. From the bar graph below, the customers who have churned have an average total day charge of about 35.18. Those customers who still have active plans with SyriaTel, have an average total day charge of 29.78.

I recommend executives brainstorm ways to retain customers that have an average total day charge of 35 dollars. Possibly creating more incentives and added perks to their phone plans could sway these customers from terminating their contracts.


#### Recommendation 3: 

The last big contributor to customer churn that I will mention is international plan. It appears roughly 42% of customers with an international plan end up churning.

I recommend  SyriaTel to further investigate into reasons why customers with international plans are highly churning. What about the current international plans are not meeting the customer's needs? 


* # Conclusion
Customers are important to any business and investing on ways to mitigate churn is crucial. Syrial Tel can employ the recommended steps to mitigate churn which will inturn increase its sales.The Customer service acknowledgement  is important and can make or break a business. The customers at Syrial Tel could be calling because they already have an issue with Syria services and whether they churn or not depends mostly on how they were handled and whether the issues were fixed. Good customer service means a better resolution and satisfaction and that will prevent a customer from churning. Customers who spend more will feel more appreciated and recognized when they are rewarded.
