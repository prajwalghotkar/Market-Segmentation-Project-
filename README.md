# Market Segmentation Project

* Marketing is crucial for the growth and sustainability of any business.
* Marketers can help build the company’s brand, engage customers, grow revenue, and increase sales.


![image](https://github.com/user-attachments/assets/38470970-5932-4798-b5dc-227328bdac1a)

* One of the key pain points for marketers is to know their customers and identify their needs.
* By understanding the customer, marketers can launch a targeted marketing campaign that is tailored for specific needs.
* If data about the customers is available, data science can be applied to perform market segmentation. 
* In this case study, you have been hired as a consultant to a bank in New York City. 
* The bank has extensive data on their customers for the past 6 months. 
* The marketing team at the bank wants to launch a targeted ad marketing campaign by dividing their customers into at least 3 distinctive groups.  

# Columns info:
1) CUSTID: Identification of Credit Card holder 

2) BALANCE: Balance amount left in customer's account to make purchases

3) BALANCE_FREQUENCY: How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)

4) PURCHASES: Amount of purchases made from account

5) ONEOFFPURCHASES: Maximum purchase amount done in one-go

6) INSTALLMENTS_PURCHASES: Amount of purchase done in installment

7) CASH_ADVANCE: Cash in advance given by the user

8) PURCHASES_FREQUENCY: How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)

9) PURCHASES_FREQUENCY: How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)

10) ONEOFF_PURCHASES_FREQUENCY: How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)

11) PURCHASES_INSTALLMENTS_FREQUENCY: How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)

12) CASH_ADVANCE_FREQUENCY: How frequently the cash in advance being paid.

13) CASH_ADVANCE_TRX: Number of Transactions made with "Cash in Advance“

14) PURCHASES_TRX: Number of purchase transactions made

15) CREDIT_LIMIT: Limit of Credit Card for user

16) PAYMENTS: Amount of Payment done by user

17) MINIMUM_PAYMENTS: Minimum amount of payments made by user  

18) PRC_FULL_PAYMENT: Percent of full payment paid by user

19) TENURE: Tenure of credit card service for user

# STEPS  

* IMPORT LIBRARIES AND DATASETS
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.preprocessing import StandardScaler, normalize
from sklearn.cluster import KMeans
from sklearn.decomposition import PCA

* Data Analysis 
  * Info()
  * Describe()

* Check who made one off purchase of approx.  $40761
* Who made cash advance of $47000 and $48000 

* VISUALIZE AND EXPLORE DATASET

  * Check for Null Values 

  * Fill up the missing elements with mean of the 'MINIMUM_PAYMENT’ 

  * Fill up the missing elements with mean of the 'CREDIT_LIMIT’ 

  * Check for Null Values – again

  * Check duplicated entries in the data

  * Drop Customer ID since it has no meaning here 

  * Create a list with number of columns 

  * Create a KDE plot with all the columns – create with for loop , iterate through all the columns in the list 

  ![image](https://github.com/user-attachments/assets/4255cbe8-fce4-4015-99cc-a83679819538)

  ![image](https://github.com/user-attachments/assets/2f122f2e-a7a9-48f1-b3dd-093ebebe1969)

  ![image](https://github.com/user-attachments/assets/ab81c86f-de02-416f-9bac-f0d50c5fb1db)

  ![image](https://github.com/user-attachments/assets/095422e9-86f9-44ef-906c-834d3bb511df)

  ![image](https://github.com/user-attachments/assets/8f5d5962-2547-49bd-a6e2-65e8f8900c6e)

 * Create Heat Map
 ![image](https://github.com/user-attachments/assets/61530b06-4ecb-4c83-8918-ebc43cce3c37)

 * Apply Feature Scaling.

 * Identify the Optimum number of clusters ( Elbow method).

 * Create the K Means Clustering Algorithm. 

 * Apply PCA in the Data Set and create clusters. 

