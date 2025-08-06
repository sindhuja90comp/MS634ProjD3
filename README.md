# Data Mining on UCI Adult Income Dataset 
- Advanced Big Data and Data Mining (MSCS-634-B01)
- #### Project Deliverable 3: Classification, Clustering, and Pattern Mining

**
## Project Overview
This project explores the UCI Adult Income dataset using classification, clustering, and association rule mining techniques. The goal is to uncover patterns related to income, education, and employment, and to discuss their practical implications.

## Key Insights

### 1. Classification
- **Models Used:** Decision Tree, Naive Bayes, and k-Nearest Neighbors (with hyperparameter tuning).
- **Findings:**
  - Decision Tree with optimized parameters achieved the best accuracy and F1 score.
  - Features such as education level, workclass, and hours-per-week were strong predictors of income category (<=50K or >50K).
  - Individuals with a Bachelor's degree or working in the private sector were more likely to have income >50K.

### 2. Clustering
- **Technique:** K-Means clustering (k=2), visualized with PCA.
- **Findings:**
  - The dataset naturally splits into two groups:
    - One group with lower education, fewer working hours, and lower income.
    - Another group with higher education, more working hours, and higher income.
  - PCA visualization confirmed clear separation between these clusters, reflecting real-world socioeconomic divisions.

### 3. Association Rule Mining
- **Technique:** Apriori algorithm on sample transactions.
- **Findings:**
  - Strong rules identified:
    - People with income >50K are often found to have a Bachelor's degree (75% confidence).
    - Those with a Bachelor's degree always (100% confidence) have income >50K.
    - People with income >50K frequently work in the private sector (75% confidence), and those in the private sector always (100% confidence) have income >50K.
  - These rules highlight strong positive associations between higher income, education, and private sector employment.

## Practical Relevance & Real-World Applications
- **Marketing:** Businesses can target premium products/services to groups with higher education and private sector jobs.
- **HR & Training:** Employers can design job roles and training programs tailored to demographics likely to yield higher income or satisfaction.
- **Policy Making:** Social programs can be better targeted to groups identified with lower income patterns, improving resource allocation.
- **Finance:** Financial institutions can customize loan or credit offers based on demographic and employment profiles that predict better repayment capacity.

## Challenges & Solutions
- **Data Cleaning:** The dataset contained missing values and categorical variables. Rows with missing values were dropped, and label encoding was used to convert categorical features to numeric.
- **Model Selection & Tuning:** Choosing the right model and hyperparameters was addressed using GridSearchCV for systematic tuning and cross-validation.
- **Interpretability:** Explaining the results of clustering and association rules required careful mapping of encoded features back to real-world categories.

## Conclusion
The project demonstrates how data mining techniques can reveal actionable insights from demographic and employment data. The findings support data-driven decision-making in business, policy, and finance.
