---
layout: post
author: Joyce
title: "Applied Data Science Project Documentation"
categories: ITD214
---
## Project Background
### Background:

IJJ Pte Ltd is a medium-sized bank headquartered in Singapore, serving a diverse clientele ranging from individual customers to small and medium enterprises (SMEs). As a growing financial institution, the bank aims to strengthen its market position by leveraging technology and data-driven strategies/insights.

### Problem Statement:

IJJ Pte Ltd struggles to attract high-value customers, optimize marketing efforts, and address customer complaints, impacting customer loyalty and business growth.

### Business Goal:

To enhance customer retention, improve marketing strategies, and effectively resolve customer complaints for better satisfaction and brand loyalty.

### Objective:
Enhance marketing performance: Implement proven marketing strategies to improve customer engagement (measured by whether a customer has signed up for term deposit in this case).

## Work Accomplished
Document your work done to accomplish the outcome

### Data Preparation

Dataset obtained from Kaggle
![image](https://github.com/user-attachments/assets/36c163ae-16a9-4b9b-8a34-0ead5d27bf45)

Original dataset: 
(marketing.csv)
![image](https://github.com/user-attachments/assets/19b2ac68-1ca7-404b-8ba5-2ccb4dbf9264)

Cleaned dataset:
![image](https://github.com/user-attachments/assets/4e7f4e6e-4503-4f29-8688-bb48ff4dd9bc)

Data exploration:
Dataset has no missing values.
Non-null count for all columns is 45211, same as total count.
![image](https://github.com/user-attachments/assets/78a8e5c3-16cf-474b-bf1c-e9c6cb9fdcb4)

Duration column:
- meaning: last contact duration, in seconds
- used box plot to see the distribution
- from here can see there is a number of outliers (at the top)
![image](https://github.com/user-attachments/assets/68e0eb77-5ef8-45a1-a45f-1c6dd71ad6a4)

Cleaning and removing outliers:
Since the number of outliers are small compared to total dataset, hence removed the rows.
![image](https://github.com/user-attachments/assets/63bea31b-7e6c-4a82-ad35-13fd88b1bf55)
![image](https://github.com/user-attachments/assets/c768198c-b512-4db3-a8b7-16812d7a2c6e)

Balance column:
- Column that indicates the average yearly balance
- Negative values is highly unlikely (unless overdraft), we will remove these values first.
![image](https://github.com/user-attachments/assets/dd3063f9-4bdb-40ed-9837-a3a396724da4)

Age column:
- Maximum and minimum age seems reasonable, 95 and 18 respectively. Hence no need to remove outliers.
- Next is to group them into 10’s for better analysis.
- Created new column age_group.

![image](https://github.com/user-attachments/assets/d6265c2b-aa4e-47c8-a371-0b7346e579a8)
![image](https://github.com/user-attachments/assets/ea56dd48-9ef6-4cbd-a916-6c579362b45e)
![image](https://github.com/user-attachments/assets/a7ce654e-40d2-4542-ad34-4d9da3e8972c)

Some values called "unknowns" in various columns (job, poutcome, contact, education), replaced them with the most frequent value.
![image](https://github.com/user-attachments/assets/c7b61ca1-bf69-467f-ac3c-67c3f6332e2b)

Target variable y (has the customer subscribed to term deposit? yes/no)

Convert it to 1 and 0:
![image](https://github.com/user-attachments/assets/d5143221-1270-457c-9ec3-11e5c3ab288b)

Apply binary encoding for columns with binary categorical values
![image](https://github.com/user-attachments/assets/15a2976b-973b-4cc6-8537-a3db1da0d930)

Apply one-hot encoding for columns with categorical variables
![image](https://github.com/user-attachments/assets/2ba42978-6980-4a73-8b9a-cb975d0e5ab1)

Apply standardization for columns with continuous variables
![image](https://github.com/user-attachments/assets/6e80f5d7-9bd7-4c55-8cc8-13c25bcd2085)

### Modelling

Selection of logistic regression as it is the simplest model.

Split the data into training and testing sets.
![image](https://github.com/user-attachments/assets/ffd4c7ab-f773-4e99-9ee0-ef7ac5c76551)

Build and train logistic regression model using sklearn
![image](https://github.com/user-attachments/assets/774384d6-7968-42a2-9a54-40fb07ed00fd)
![image](https://github.com/user-attachments/assets/d4ef9967-a4f9-4bf8-a575-980650c79e41)

### Evaluation
Model is overall 90% accurate.
The model is performing well with class 0, achieving high precision (0.91), recall (0.97), and F1-score (0.94).
However, the model struggles with class 1, where precision is 0.65, recall is 0.34, and the F1-score is 0.44. This suggests the model is not capturing enough of the positive cases (1s) and is making a significant number of false negatives (725).
Might be imbalance, use over/ under sampling

![image](https://github.com/user-attachments/assets/86a6f41d-f7f9-4001-b5b4-35b09bf6e259)
![image](https://github.com/user-attachments/assets/92cdc90b-4a9d-4229-a54a-c3f9012e7d85)
![image](https://github.com/user-attachments/assets/d006713c-a969-4835-bc54-76ce3e3dec38)

![image](https://github.com/user-attachments/assets/71f32ab5-7f07-400c-b465-586683632098)
![image](https://github.com/user-attachments/assets/9c0f6d0c-3342-4ffe-aa76-a0ffddeeba9d)
![image](https://github.com/user-attachments/assets/22d1839c-f41a-49cf-9727-49654448c691)


## Recommendation and Analysis
![image](https://github.com/user-attachments/assets/61c1bf26-7a15-459b-b7d5-918e024ed64b)

### Suggested marketing campaign: 
### More calls for longer duration in the month of march to get higher engagement rates.
![image](https://github.com/user-attachments/assets/647a2651-ac62-4636-bde6-1e3b6c9b3d48)

## AI Ethics
Discuss the potential data science ethics issues (privacy, fairness, accuracy, accountability, transparency) in your project. 

### Privacy:
The data collection and storage of personal, sensitive or confidential data should be properly handled to ensure there is no data leakage. One method would be to anonymize or aggregate the data such that the data cannot be tied back to any individual. Which we have seen in our case, where there is no PII data. 

During the data collection process, users should have a clear understanding of what is collected and how the data will be used, as well as the potential risks before consenting to the data collection.

As a rule of thumb, only relevant data should be collected, no more than necessary and kept no longer than needed. Data retention longer than required may pose privacy risks.

### Fairnesss:

Ensure the model is not biased, which may potentially disadvantage certain groups . For example, in Amazon where their model for recruitment was discrimatory against females. In the current model, ensure there is balanced dataset across different jobs (management, technician, entrepreneur, blue-collar), and marital status (single, married, divorced) to ensure differnt demographics are represented fairly in the model.

### Accuracy:

Data quality is essential to obtain good and accurate insights. Low-quality, incomplete or noisy data can lead to inaccurate predictions. The data pre-processing step is essential, for example, removing outliers and null values. 

Model accuracy vs interpretability should be considered. Models can be highly accurate but difficult to interpret and hard to understand how decisions are made which can lead to a lack of trust or accountability in the results. 

### Accountability:

For models which have high risk and high unpredictability, there should be human in the loop. There should also be clear responsiblility assignment for model decisions and ensure that errors are rectified quickly.

### Transparency:

Complex "black box" models such as deep learning makes it hard to see how the model arrive at specific decision. This lack of transparency can undermine trust and make it difficult for stakeholders to understand or challenge the results. 

There should be transparency in where the data is coming from and what biases exists in the data anad how it has been processed.

Clear documentation and communication about how decisions are made by models are required for high-stake areas like criminal justice or lending are essential to build trust.

## Source Codes and Datasets
Upload your model files and dataset into a GitHub repo and add the link here. 
