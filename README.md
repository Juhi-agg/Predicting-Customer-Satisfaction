# Predicting-Costomer-Satisfaction

Cognizance is a Technical Fest of IIT Roorkee. We participated in a Data Competition Alankan. <br>
The problem Statment is uploaded along with dataset and competition guidelines. <br>

The case study revolves around Invistico Airlines and its growing customer base over the past few years. As the head of the Business Insights Department, we had to: 
<br> 1. Build a model to predict customer satisfaction 
<br> 2. Identify top factors affecting the customer satisfaction 

We followed a PPDAC structure to approach the problem. PPDAC stands for Problem-Plan-Data-Analysis-Conclusion. 

<b>Step 1: Problem</b> <br>
Before arriving at a solution, it is important to understand the question well. As per the problem statement, Invistico Airlines strategizes to keep operation costs low and customer satisfaction high. In this analysis, we’ll be helping Invistico Airlines in the latter. 

<b>Step 2: Plan </b> <br>
It is important to plan a case study before execution. Our planning began with brainstorming sessions amongst the team members. After initial discussions, we came up with the following action plan: 

Exploratory data analysis ---> Feature Selection ---> Model Training & Optimisation ---> Analyse the results 

<b>Step 3: Data</b>
<br>
<u>3.1 Understanding Customers:</u> To solve a business problem, we need to understand its customers. On exploring the data, we found that 
<br> -  51% of the customers are female while 49% comprises the male.
<br> - 60% of the customers are from the age bracket 22-49 yrs.
<br> - Business Class Travel is preferred slightly more than Eco Class while Eco+ is used only by 7% of the customers.
<br> - 82% of the flyers were loyal to the airlines.
<br> <br>
3.2 Factors affecting customer satisfaction: The color scaled graph below shows the relationship between customer satisfaction and features (like Seat Comfort etc.). As mentioned in the problem statement, 1 represents the Least satisfied, and 5 represents the Most satisfied. For the sake of analysis, we have assumed that scores 1 & 2 represents “Dissatisfaction” and 4 & 5 represents “Satisfaction”. Score 3 was assumed to be neutral and hence not considered for analysis. 
<br>


3.3. Other key insights:
People traveling in Business Class are more satisfied 
Most of the people traveling in Economy class are dissatisfied
For business purposes travel, customers traveling via Eco or Eco+ are more dissatisfied than those traveling via Business Class. 
In the case of personal travel, no such pattern was observed. Customers traveling via Business, Eco, or Eco+ are equally satisfied.
Flight distance vs Satisfaction
<br>
3.4 Feature Selection: Before training our model it is essential to select critical features and remove highly correlated ones. Using Chi-Square, mutual interaction, and heatmap analyses, we deduced that the following features are redundant:
Arrival Delay in minutes: Highly correlated with Departure delay in minutes 

The following features were dropped due to low scores: 
<br>- Gender
<br>- Gate location
<br>- Type of travel
<br>- Departure/Arrival time convenient 
<br><br>
<b>Step 4: Analysis</b>  

4.1 Model Building: The problem in hand demands the use of supervised classification techniques to model the relation of the predictor variables with the output variable. 
We used the Logistic Regression, kNN, SVM, Random Forest and XGBoost models along with optimization techniques for tuning the models

4.2 Model Selection and Evaluation Metrics: Random Forest Classifier resulted in maximum accuracy of 94% and an f1-score of 0.94. This model can be further optimized using the Grid Search algorithm to find out the optimal hyperparameters. 

<b>Step 5: Conclusion</b> 

Predicting customer satisfaction: We deployed a generic random forest classification model which resulted in an accuracy of 94% to predict customer satisfaction. Redundant features such as gate location, gender, type of travel, etc. were excluded from the model due to reasons explained above. 

Top factors affecting customer satisfaction: Upon diligent analysis, we found out the top 5 factors affecting customer satisfaction/dissatisfaction. 

Satisfaction: Cleanliness, Baggage Handling, Inflight Entertainment, Online Support, On-Board Service   
Dissatisfaction: Seat Comfort, Food and drink, Inflight wifi service, Gate Location, Departure/Arrival time convenient






