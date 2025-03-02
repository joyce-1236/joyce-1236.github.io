---
layout: post
author: Name
title: "Applied Data Science Project Documentation"
categories: ITD214
---
## Project Background
An overview of the project business goals and objectives. 

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


### Modelling
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit. Proin convallis mi ac felis pharetra aliquam. Curabitur dignissim accumsan rutrum. In arcu magna, aliquet vel pretium et, molestie et arcu. Mauris lobortis nulla et felis ullamcorper bibendum. Phasellus et hendrerit mauris. Proin eget nibh a massa vestibulum pretium. Suspendisse eu nisl a ante aliquet bibendum quis a nunc. Praesent varius interdum vehicula. Aenean risus libero, placerat at vestibulum eget, ultricies eu enim. Praesent nulla tortor, malesuada adipiscing adipiscing sollicitudin, adipiscing eget est.

### Evaluation
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit. Proin convallis mi ac felis pharetra aliquam. Curabitur dignissim accumsan rutrum. In arcu magna, aliquet vel pretium et, molestie et arcu. Mauris lobortis nulla et felis ullamcorper bibendum. Phasellus et hendrerit mauris. Proin eget nibh a massa vestibulum pretium. Suspendisse eu nisl a ante aliquet bibendum quis a nunc. Praesent varius interdum vehicula. Aenean risus libero, placerat at vestibulum eget, ultricies eu enim. Praesent nulla tortor, malesuada adipiscing adipiscing sollicitudin, adipiscing eget est.

## Recommendation and Analysis
Explain the analysis and recommendations

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit. Proin convallis mi ac felis pharetra aliquam. Curabitur dignissim accumsan rutrum. In arcu magna, aliquet vel pretium et, molestie et arcu. Mauris lobortis nulla et felis ullamcorper bibendum. Phasellus et hendrerit mauris. Proin eget nibh a massa vestibulum pretium. Suspendisse eu nisl a ante aliquet bibendum quis a nunc. Praesent varius interdum vehicula. Aenean risus libero, placerat at vestibulum eget, ultricies eu enim. Praesent nulla tortor, malesuada adipiscing adipiscing sollicitudin, adipiscing eget est.

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
