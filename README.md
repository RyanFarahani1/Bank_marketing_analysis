# Bank Marketing Campaign Dataset

## Abstract
This repository contains data from direct marketing campaigns (via phone calls) conducted by a Portuguese banking institution. The primary goal is to predict whether a client will subscribe to a term deposit (`y`).

## Dataset Overview
The dataset captures information from multiple marketing campaigns, often requiring more than one contact with the same client to determine whether the term deposit was subscribed (`yes`) or not (`no`).  

The full dataset `bank-additional-full.csv` contains **41,188 records** with **20 input features**, ordered chronologically from May 2008 to November 2010. Smaller subsets are also available for testing computationally intensive machine learning algorithms such as SVM.

The classification target is `y`, indicating whether a client subscribed to a term deposit.

## Attributes

### Bank Client Data
1. **age**: Numeric  
2. **job**: Type of job (categorical: `'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown'`)  
3. **marital**: Marital status (categorical: `'divorced','married','single','unknown'`; note: `'divorced'` includes divorced or widowed)  
4. **education**: Education level (categorical: `'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown'`)  
5. **default**: Has credit in default? (categorical: `'no','yes','unknown'`)  
6. **housing**: Has housing loan? (categorical: `'no','yes','unknown'`)  
7. **loan**: Has personal loan? (categorical: `'no','yes','unknown'`)  

### Contact Data (Last Campaign)
8. **contact**: Contact communication type (categorical: `'cellular','telephone'`)  
9. **month**: Last contact month of the year (categorical: `'jan', 'feb', ..., 'dec'`)  
10. **day_of_week**: Last contact day of the week (categorical: `'mon','tue','wed','thu','fri'`)  
11. **duration**: Last contact duration in seconds (numeric). **Important**: This feature strongly influences the target variable. Duration is not known before the call and should be excluded for realistic predictive modeling; it is mainly for benchmarking purposes.  

### Campaign Information
12. **campaign**: Number of contacts performed during this campaign for this client (numeric, includes last contact)  
13. **pdays**: Days since last contact from a previous campaign (numeric; `999` means client was not previously contacted)  
14. **previous**: Number of contacts performed before this campaign for this client (numeric)  
15. **poutcome**: Outcome of the previous marketing campaign (categorical: `'failure','nonexistent','success'`)  

### Social and Economic Context
16. **emp.var.rate**: Employment variation rate - quarterly indicator (numeric)  
17. **cons.price.idx**: Consumer price index - monthly indicator (numeric)  
18. **cons.conf.idx**: Consumer confidence index - monthly indicator (numeric)  
19. **euribor3m**: Euribor 3 month rate - daily indicator (numeric)  
20. **nr.employed**: Number of employees - quarterly indicator (numeric)  

### Target Variable
21. **y**: Has the client subscribed to a term deposit? (binary: `'yes','no'`)  

## Acknowledgements
This dataset is publicly available for research purposes. For further details, refer to:

**Moro et al., 2014**  
S. Moro, P. Cortez, and P. Rita. *A Data-Driven Approach to Predict the Success of Bank Telemarketing.* Decision Support Systems, Elsevier, 62:22-31, June 2014.  

**Data Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/bank+marketing)
