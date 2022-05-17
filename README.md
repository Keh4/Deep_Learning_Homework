Deep Learning – Charity Effectiveness Model

Overview: The purpose of this analysis was to create an algorithm for Alphabet Soup to predict the success of their applicants cause with their provided funds. 

Results: My code resulted in 80% accuracy after optimization
Data Preprocessing 
	•	Target for model = IS_SUCCESSFULL
	•	Features for model:
		o	NAME—Name of Charity 
		o	APPLICATION_TYPE—Alphabet Soup application type 
		o	AFFILIATION—Affiliated sector of industry 
		o	CLASSIFICATION—Government organization classification 
		o	USE_CASE—Use case for funding 
		o	ORGANIZATION—Organization type 
		o	STATUS—Active status 
		o	INCOME_AMT—Income classification 
		o	SPECIAL_CONSIDERATIONS—Special consideration for application 
		o	ASK_AMT—Funding amount requested
	•	Variables Removed = EIN 
	•	Variables Adjusted for Model Performance:
		o	NAME – Binned to compile those that appear less than 6 times into “Other”
		o	APPLICATION_TYPE - Binned to compile those that appear less than 500 into “Other”
		o	CLASSIFICATION - Binned to compile those that appear less than 500 into “Other”
		o	ASK_AMT – Removed outliers identified as those asking for $1 Million dollars or more.

Compiling, Training, and Evaluating the Model 
	•	After optimization, I used four hidden layers with decreasing neurons with each for more focus.
	•	I choose RELU as it is simple and fast. RELU is also used most in the teaching examples.
	•	Target model performance was achieved 80%  
	•	Steps to increase model performance were as follows: 
		o	Added Name as a Feature to capture patterns for charities that had multiple rows. 
		o	Took the outliers out of the Asked amount.  Looking at only those below $1M after noticing some were in the billions. My assumption is those were mistakes.
		o	I started with two hidden layers and added two more for a total of 4 with added neurons from the original code.

Summary:  Overall the results of the model were that it performed well in predicting whether a charity would use the money provided to them by Alphabet Soup effectively.  I would recommend developing another model that would predict ROI for Alphabet funds.  I would investigate the amount asked by Charity and gather more detailed data around the level of effectiveness by quantifying.
