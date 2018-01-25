# Relax Project

Objective: 
* From two data sets on behavior of 12000 users who signed up for the product in 2 years:
 ** Define a variable adopted user representing a user who logs into the system for 3 consecutive days within a 7 day window
 ** Identify which factors predict future user adoption
 
 Strategy:
** introducing the Data Set
** data wrangling 
   ** data manipulation
   ** data exploration
   ** filling missing values
   ** generate target variable: adopted user
   ** Determine predictors
   ** Example prediction

** Result**
**Target variable: *"adopted_user"**

**Predictors:**
Visited_Count : the number of times a user logged in to the site
adopted-user-visit_Count : the number of times a user logged in 3 consecutive days within 7 days period
creation time : time of first login
creation_source : how users account was created
last_session_creation_time : unix timestamp of last login
opted_in_to_mailing_list : whether they have opted into receiving marketing e-mails
enabled_for_marketing_drip : whether they are on the regular marketing email drip
org_id : the organization they belong
invited_by_user_id : which user invited them to join

**Example: Predict adopted user from org_id**
* Use Logistic Regression / Classification
* Use Kfold cross validation and Grid Search CV to determine the best regularization parameter (for model tuning)
* Generate the accuracy score.

Accuracy Score = 82%
* Since the accuracy score for our model is 82%, it suggests that the risk that a portion of the sample is misclassified is 18%
