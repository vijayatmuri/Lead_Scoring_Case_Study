# Lead_Scoring_Case_Study
Lead Scoring Case Study
# Problem Statement
An education company named X Education sells online courses to industry professionals. On any given day, many professionals who are interested in the courses land on their website and browse for courses. 

The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%. 
 
Now, although X Education gets a lot of leads, its lead conversion rate is very poor. For example, if, say, they acquire 100 leads in a day, only about 30 of them are converted. To make this process more efficient, the company wishes to identify the most potential leads, also known as ‘Hot Leads’. If they successfully identify this set of leads, the lead conversion rate should go up as the sales team will now be focusing more on communicating with the potential leads rather than making calls to everyone

# Problem Mapping and Solution Approach
The company requires you to build a model wherein you need to assign a lead score to each of the leads such that the customers with a higher lead score have a higher conversion chance and the customers with a lower lead score have a lower conversion chance. The CEO has given a ballpark of the target lead conversion rate to be around 80%.

The problem can be mapped to find the hot leads i.e. the leads that are most likely to convert into paying customer.
This is a classification problem, where in we need to build a model to assign lead score to each of the leads such that the customer with higher lead score has higher conversion chance and customer with lower lead score has lower conversion chance
The company wants to utilize their resources optimally such that the lead conversion rate to be around 80% (we need to have suitable cutoff of the lead score and identify the potential leads such that lead conversion rate (recall_score) would be greater than 80%)

# Data Preparation
Performed EDA Analysis, Missing Values and Outlier are treated
The underlying patterns between the variables are identified and arrived at intital hypothesis.
Converted binary variables (Yes/No)  to 0/1, for the columns 'Do Not Email', 'Through Recommendations', 'A free copy of Mastering The Interview’
For categorical variables with multiple levels, created dummy features (one-hot encoded)
Created a new variable - Average time spent as (Total Time Spent on Website / TotalVisits) and dropped these two columns
The dataset was split into train (70%) and test(30%) using sklearn.model_selection.train_test_split
Some of the columns have a different value ranges compared to other binary, dummy variables. Performed Feature Scaling using MinMaxScaler() for the columns 'Average Time Spent on Website','Page Views Per Visit’ and performed scalar.fit_transform() on training data set.
Dropped highly correlation dummy variables as observed for correlation matrix

# Model Building
We have used statsmodels.api and GLM model for binomial families to build the model, provides more detailed statistical output, including parameter estimates, standard errors, p-values, confidence intervals, and model fit statistics like AIC and BIC. This can be useful for statistical inference and interpretation.
After creating dummy variables, we have around 97 features that are fed into the model. This may lead to over fitting and multi-collinearity. And also, difficult to interpret the important features.
We have then proceeded with Feature Selection using Recursive Feature Elimination (RFE) and selected 25 features for further model building
We continued with the further feature elimination using the top to bottom approach, where in we eliminated the feature based on higher p-values (lower significance) and high VIF value (high multi-collinearity)


# Model Evalaution
The Model is evaluated using the ROC Curve, Precision and Recall scores.
Optimum cut-off value is arrived by plotting the Precision_Recall_Curve
Further model performance was evaluated on unseen data using cross validation technique

# Model Prediction and Recommendation
The Model is applied on the test data set and Lead Score is predicted
The performance metrics on test data set as in range with that of taining data set, indicating the model is not overfitting
Further Gain Chart, KS - statistics are calculated and recommendation are provided to the business



