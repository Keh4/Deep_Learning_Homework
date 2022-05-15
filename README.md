# Deep_Learning_Homework

1.	Overview: The purpose of this analysis was to create an algorithm for Alphabet Soup to predict the success of their applicants cause with their provided funds. 

2.	Results: Our code resulted in 80% accuracy after optimization
•	Data Preprocessing 
o	Target for model = IS_SUCCESSFULL
o	Features for model:
• NAME—Name of Charity 
• APPLICATION_TYPE—Alphabet Soup application type 
• AFFILIATION—Affiliated sector of industry 
• CLASSIFICATION—Government organization classification 
• USE_CASE—Use case for funding 
• ORGANIZATION—Organization type 
• STATUS—Active status 
• INCOME_AMT—Income classification 
• SPECIAL_CONSIDERATIONS—Special consideration for application 
• ASK_AMT—Funding amount requested
o	Variables Removed = EIN 
o	Variables Adjusted for Model Performance:
	NAME – Binned to compile those that appear less than 6 times into “Other”
	APPLICATION_TYPE - Binned to compile those that appear less than 500 into “Other”
	CLASSIFICATION - Binned to compile those that appear less than 500 into “Other”
	ASK_AMT – Removed outliers identified as those asking for $1 Million dollars or more.
	
•	Compiling, Training, and Evaluating the Model 
o	After optimization, I leveraged four hidden layers with decreasing neurons with each for more focus. I choose RELU as it is simple and fast. RELU is also used most in the teaching examples.
o	The target model performance was achieved 80%  
o	Steps to increase model performance were as follows: 
	Added Name as a Feature to capture patterns for charities that had multiple rows. 
	Took the outliers out of the Asked amount.  Looking at only those below $1M after noticing some were in the billions. My assumption is those were mistakes.
	I started with two hidden layers and added two more for a total of 4 with added neurons.  
