# Relax Project

Objective: 
* From two data sets on behavior of 12000 users who signed up for the product in 2 years:
 * Define a variable adopted user representing a user who logs into the system for 3 consecutive days within a 7 day window
 * Identify which factors predict future user adoption
 
 Strategy:
* introducing the Data Set
* data wrangling 
   * data manipulation
   * data exploration
   * filling missing values
   * generate target variable: adopted user
   * Determine predictors
   * Example prediction

Result:
* Target variable: *"adopted_user"

* Predictors:
 1. Visited_Count : the number of times a user logged in to the site
 2. adopted-user-visit_Count : the number of times a user logged in 3 consecutive days within 7 days period
 3. creation time : time of first login
 4. creation_source : how users account was created
 5. last_session_creation_time : unix timestamp of last login
 6. opted_in_to_mailing_list : whether they have opted into receiving marketing e-mails
 7. enabled_for_marketing_drip : whether they are on the regular marketing email drip
 8. org_id : the organization they belong
 9. invited_by_user_id : which user invited them to join

Example: Predict adopted user from org_id
* Use Logistic Regression / Classification
* Use Kfold cross validation and Grid Search CV to determine the best regularization parameter (for model tuning)
* Generate the accuracy score.

Accuracy Score = 82%
* Since the accuracy score for our model is 82%, it suggests that the risk that a portion of the sample is misclassified is 18%
