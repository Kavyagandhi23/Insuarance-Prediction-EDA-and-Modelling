# Health Insurance Cross-Sell Prediction 

## Project Overview:
This project aims at an insurance company, predicting the likelihood of existing health insurance policyholders showing interest in the company's vehicle insurance offerings. By leveraging demographic information, vehicle details, and policy-related data, we intend to build a predictive model that will help optimize the company's communication strategy and enhance revenue generation.

## Problem Statement:
The primary goal is to develop a machine learning model capable of predicting whether a customer, who has previously purchased health insurance, would also be interested in purchasing vehicle insurance. This prediction will be based on various features such as gender, age, region code, vehicle age, damage history, premium amount, and the sourcing channel.

## Dataset Description:

Columns       | Description         |
--------------|---------------------|
ID   | Unique ID for the Customer  |
Gender | Gender of Customer |
Age | Age of the Customer |
Driving_License | 0 : Customer does not have DL, 1 : Customer already has DL |
Region_Code	| Unique code for the region of the customer |
Previously_Insured	| 1 : Customer already has Vehicle Insurance, 0 : Customer doesn't have Vehicle Insurance | 
Vehicle_Age	| Age of the Vehicle | 
Vehicle_Damage	| 1 : Customer got his/her vehicle damaged in the past. 0 : Customer didn't get his/her vehicle damaged in the past. |
Annual_Premium	| The amount customer needs to pay as premium in the year |
Policy_Sales_Channel	| Anonymized Code for the channel of outreaching to the customer ie. Different Agents, Over Mail, Over Phone, In Person, etc. |
Vintage	| Number of Days, Customer has been associated with the company |
Response	**(LABEL)** | 1 : Customer is interested, 0 : Customer is not interested | 


## Flow of Decision Modelling:  

The Project will follow a standard machine learning pipeline, encompassing the following key steps:

1. Data Exploration & Preprocessing:
2. Exploratory Data Analysis (EDA):
3. Feature Selection:
4. Model Development:
5. Model Evaluation:
6. Communicating Strategy Recommendations:

## Model Evaluation Metric:

Model         | Accuracy      | F1_Score | Comments | 
--------------|---------------|----------|----------|
K-Mean        | 74%      | 15%         | K-Means shows moderate accuracy and a relatively higher F1 score, indicating a decent balance between precision and recall. |
COPOD Anamoly Detection        | 76%   | 13% | Copod performs slightly better than K-Means in terms of accuracy but exhibits a lower F1 score, suggesting potential challenges in correctly identifying positive instances. |
logistic Regression | 87% | 6% | Logistic Regression demonstrates high accuracy but a notably low F1 score. This suggests a potential imbalance in class distribution or challenges in capturing true positive instances. | 
LightGBM Classifier | 88% | 5% | While LightGBM achieves high accuracy, the extremely low F1 score raises concerns about its ability to effectively identify positive cases. Further tuning may be required to enhance performance. |
XGB CLassifier      | 76% | 45% | XGBoost shows a balanced performance with good accuracy and a high F1 score, indicating effective precision and recall. This model appears promising for the task. |
Random Forest       | 88% | 0% | Despite high accuracy, the F1 score being zero suggests that Random Forest might struggle to identify positive instances. Further investigation and parameter tuning are recommended. |
Keras Sequential Model | 68% | 42% | Keras Sequential exhibits relatively lower accuracy but a higher F1 score. This suggests that while it may not predict all instances accurately, it performs well in correctly identifying positive cases. |

> For a balanced approach, XGBoost seems to offer a good trade-off between accuracy and F1 score. However, further refinement and fine-tuning are crucial to enhance the model's performance and reliability in predicting customers interested in vehicle insurance.
 
## Dependencies:

* Python 3.6+
* ML Libraries: scikit-learn, tensorflow, numpy and pandas

## Run the Notebook:

1. Clone the Repository:
<code> git clone https://github.com/your-username/Insurance-Cross-Sell-Prediction.git
cd Insurance-Cross-Sell-Prediction </code>

2. Install Dependencies:
<code> pip install -r requirements.txt </code>

3. Run the python/ jupyter notebook file:
<code> Run insurance_predictive.py </code>

