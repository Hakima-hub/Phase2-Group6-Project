#PHASE3_PROJECT 

##Problem Defination

SyriaTel wants to predict customer churn using historical data. Additionally, they want to quantify the financial losses incurred by long-term customers who leave the service.


##Business Understanding

SyriaTel, a TelecommunicationsCompany is concerned about customer churn the phenomenon where customers stop using their services. Some long-term customers may generate lower revenue while still incurring service costs, potentially leading to revenue losses. Understanding the characteristics of customers who are likely to churn will help the company take preventive measures.

##Data Preprocessing
This section prepare the provided bigml data for analysis. We intend to do the following:

###Dataset Overview - Load and understand the data
Handling Missing Values using derived domain knowledge and imputation
Data Cleaning e.g. standardizing categorical values, deriving useful date data, removing duplicates etc
Dataset Overview
It is imperative for us to understand the bigml dataset first i.e.:

The data structure e.g. available tables, their columns, data types and presence of missing values
Establish the relevance of the data to our study
Identify useful columns to focus on
Data Understanding will prescribe subsequent cleaning steps to be done in the Data Cleaning subsection

###Python Libraries Initialization

First, we initialize common libraries we project to utilize in this exercise:

pandas to create and manipulate dataframes
seaborn and matplotlib to facilitate any requisite visualizations within the notebook
numpy for mathematical calculations
scikit-learn to provide tools for machine learning models, feature scaling, train-test-split and evaluation metrics.
etc
Data Loading

We then load the dataset into python as a dataframe and embark on a data understanding exercise.

###Data Understanding



###Exploratory Data Analysis

We used Tableau to explore the data and established the following insights:

churn distribution
The majority of the customers do not curn indicating an imbalanced dataset.
![alt text](image-3.png)

Account length distribution for churned and non churned customers:

Both churn and non churned customers exist across various account lengths which shows that longer account lenngths result in churn.
![alt text](image-4.png)

correlation heatmap

churn is highly correlated with customer service calls which indicates that Customers who makes more service calls are more likely to churn.
![alt text](image-5.png)


##Conclusion
 1. Customer services calls are strongly correlated with churn which indicates customers who make more calls to customer service are more likely to leave this suggests dissatisfaction with SyrialTel's support services.

2. call usage has weak correlation with churn this might be as a result of service quality and pricing.

3. All the model had the same recall of 74% which means all the model detected most of the customers who actually churned.

##Recommendation

 Improve customer support by identifying common customer complaints from high frequently callers.

2. Enhance customer engagement by offering customer support for those making frequent service calls.

3.Handle class imbalance by using techniques like class weight to improve model accuracy since the churned customer are fewer.

4. The best model was Decision Tree Model with 92% accuracy and precision of 74%.

5. If the company wants to catch churners they should increase recall to 80-85 or even 90%.
