# Market Segmentation Project
--
**Understanding customer segments is vital for businesses aiming to launch targeted marketing campaigns, improve engagement, and maximize revenue growth. This project applies data science to customer data from a New York City bank to identify at least three actionable customer groups for targeted advertising.**
![image](https://github.com/user-attachments/assets/448feb12-117d-4b89-a33b-20e9b318dc68)

--

##### Project Overview
- **Objective**: Segment bank customers into distinct groups based on behavioral and financial data, enabling precise and impactful marketing.
- **Context**: Consultant role for a bank possessing 6 months of customer data. The marketing team seeks to identify segments for campaign targeting.

--

**Understanding customers is at the heart of effective marketing. In this project, you take the role of a consultant for a New York City bank aiming to improve its marketing strategy through data-driven customer segmentation. The bank possesses six months of detailed customer data and wishes to optimize their advertising campaigns by targeting specific groups with tailored messages and offers.**

##### Project Context and Purpose
- **Business Importance**: Marketing fuels a company’s long-term growth by building brand identity, engaging customers, increasing revenue, and driving sales.
- **Key Challenge**: Marketers need to identify and understand their customers’ unique needs to design highly effective campaigns.
- **Solution with Data Science**: When customer data is available, methods like clustering and segmentation become powerful tools for grouping people with similar behaviors or needs.
- **Project Scenario**: Prajwal,You as a data science consultant, are brought in to analyze the bank’s customer data. The marketing team’s goal is to divide their customer base into at least three distinct segments to enable more targeted and relevant advertising.

--

#### What This Project Involves
- **Data Collection**: Analyze six months of data representing customer transaction and behavior patterns.
- **Segmentation**: Use data science (typically clustering algorithms like KMeans) to group customers based on similarities in their financial behaviors and preferences.
- **Outcome**: Identify and describe at least three unique customer segments the bank can target with personalized marketing campaigns.

--

##### Why It Matters
- **For the Bank**: Enables more efficient and effective allocation of marketing efforts and budget, boosts customer engagement, and increases the likelihood of campaign success.
- **For Customers**: Ensures they receive offers and communication tailored to their actual needs and preferences, enhancing satisfaction and loyalty.

--

##### 1. Dataset Description
###### Each row represents a customer, with the following features:
- **CUSTID**: Unique credit card holder ID
- **BALANCE**: Remaining account balance available for purchases
- **BALANCE_FREQUENCY**: Frequency score (0–1) for balance updates
- **PURCHASES**: Total purchase amount
- **ONEOFF_PURCHASES**: Maximum one-time purchase
- **INSTALLMENTS_PURCHASES**: Total of purchases made in installments
- **CASH_ADVANCE**: Total cash withdrawn in advance by the customer
- **PURCHASES_FREQUENCY**: Regularity of purchases (0–1)
- **ONEOFF_PURCHASES_FREQUENCY**: Frequency of one-off purchases (0–1)
- **PURCHASES_INSTALLMENTS_FREQUENCY**: Frequency of installment purchases (0–1)
- **CASH_ADVANCE_FREQUENCY**: Frequency of cash advances (0–1)
- **CASH_ADVANCE_TRX**: Number of cash advance transactions
- **PURCHASES_TRX**: Number of purchase transactions
- **CREDIT_LIMIT**: Card’s credit limit
- **PAYMENTS**: Total payments made
- **MINIMUM_PAYMENTS**: Minimum payments made
- **PRC_FULL_PAYMENT**: Percent of full payment made
- **TENURE**: Card membership period (months)

--

##### 2. Systematic Step-by-Step Process
- Step 1: Import Libraries and Datasets
  - Import essential libraries:
    - pandas, numpy for data handling.
    - matplotlib, seaborn for visualization.
    - sklearn for machine learning (StandardScaler, KMeans, PCA).

- Step 2: Data Analysis
  - Load the dataset.
  - Use .info() and .describe() to understand data structure and statistics.
  - Identify special cases (e.g., check who made a one-off purchase of ~$40,761, and who took cash advances of ~$47,000/$48,000).

- Step 3: Visualize and Explore Dataset
  - Explore distributions and patterns of key numerical columns with visualizations:
    - KDE plots for each feature.
    - Histograms for overall spread.
  - Identify outliers and trends in purchase/advance amounts.

- Step 4: Handle Missing Data
  - Check for missing/null values.
  - Impute missing ‘MINIMUM_PAYMENTS’ and ‘CREDIT_LIMIT’ with their respective means.
  - Verify that no null values remain after imputation.

- Step 5: Clean Data
  - Check for duplicated entries.
  - Drop CUSTID column (not analytically useful).
  - Generate a list of feature columns for further analysis.

- Step 6: Exploratory Data Analysis (EDA)
  - Loop through columns to plot KDE (Kernel Density Estimation) plots for each, visualizing the probability distribution.
  ![image](https://github.com/user-attachments/assets/4255cbe8-fce4-4015-99cc-a83679819538)
  ![image](https://github.com/user-attachments/assets/2f122f2e-a7a9-48f1-b3dd-093ebebe1969)
  ![image](https://github.com/user-attachments/assets/ab81c86f-de02-416f-9bac-f0d50c5fb1db)
  ![image](https://github.com/user-attachments/assets/095422e9-86f9-44ef-906c-834d3bb511df)
  ![image](https://github.com/user-attachments/assets/8f5d5962-2547-49bd-a6e2-65e8f8900c6e)

  - Generate a heat map of feature correlations.
  ![image](https://github.com/user-attachments/assets/61530b06-4ecb-4c83-8918-ebc43cce3c37)

- [imageageStep 7: Feature Scaling
  - Apply StandardScaler to normalize features—crucial for clustering algorithms like KMeans.

- Step 8: Optimal Number of Clusters
  - Use the Elbow Method:
    - Plot the inertia (within-cluster sum of squares) for a range of cluster numbers.
    - Identify the "elbow point" where additional clusters yield diminishing returns on reduced inertia.

- Step 9: KMeans Clustering
  - Train the KMeans algorithm using the optimal cluster number.
  - Assign each customer to a segment based on clustering results.

- Step 10: Dimensionality Reduction (PCA)
  - Apply PCA for visualization:
    - Reduce multidimensional feature space to 2–3 principal components.
    - Visualize cluster separations and centroids in 2D/3D plots.

##### 3. Key Deliverables
- Segmented customer groups, each with unique spending and payment behavior.
- Reactively visualized clusters (PCA plot, cluster centers).
- Interpretations of segment profiles for actionable marketing targeting.

##### 4. Tools & Tech Stack
- Languages: Python
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn
- Environment: Jupyter Notebook / VS Code

##### 5. How to Run
- 1) Place the data CSV in the project directory.
- 2) Install dependencies via requirements.txt:


   ```
   pip install -r requirements.txt
   pandas
   numpy
   matplotlib
   seaborn
   scikit-learn
   jupyter
  ```
- 3) Run the Jupyter Notebook or the main Python script following section labels.

---

##### Benefits of Your Market Segmentation Project

- **Improved Marketing ROI**:By dividing customers into distinct segments, the bank can create targeted marketing campaigns. This ensures advertisements and offers reach the most relevant audiences, leading to higher engagement rates, increased conversion, and better returns on marketing investment.

- **Better Understanding of Customer Needs**:Clustering reveals underlying differences in spending, credit usage, and payment behaviors. Marketers and product managers gain deep insights into each segment’s specific needs, habits, and preferences.

- **Personalized Customer Experience**:Enables the bank to tailor its services, recommendations, and credit products for each segment. Personalization typically boosts customer satisfaction and loyalty.

- **Efficient Resource Allocation**:Resources (campaign budget, staff, time) can be strategically allocated to segments with the highest growth or profit potential, minimizing wastage and maximizing business impact.

- **Data-Driven Strategy**:Your project demonstrates advanced use of Python, clustering algorithms (KMeans), and dimensionality reduction (PCA), setting a strong precedent for data-driven decision-making in business.

- **Competitive Advantage**:By uncovering less obvious customer niches (e.g., installment buyers vs. heavy cash-advance users), the bank can offer specialized promotions or products, strengthening its position in the financial market.

- **Risk Reduction**:Identifying segments with risky behaviors (such as frequent cash advances or consistently low payments) helps the bank proactively manage credit risk, design safer products, or implement preemptive interventions.

- **Scalability and Reusability**:The project’s workflow is modular and can be applied to other banks, geographies, or industries—anywhere segmentation is needed.

- **Enhanced Communication**:Clarity in data visualization and customer profiles assists non-technical stakeholders in understanding complex customer landscapes. This improves communication between data teams, marketers, and executives.

##### By Prajwal Ghotkar 
