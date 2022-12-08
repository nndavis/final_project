##  can we rate a job's value? - Project Outline

## Team
-  Adio Olufemi Peter
- Ashlesha Vengareddy
- Noah Davis
- Ethan Dirksen

## Why "can we rate a job's value?"
As we are finishing bootcamp and about to start looking for jobs. We wanted know what companies and jobs will be good to look for and what features would be best to 
consider while looking for jobs and which companies are best to be considered. The topic  was relevant for all of us and  could prove beneficial to find employement.

Questions we want answered:
does location adversely affect diversity inclusion?
are managers bias in their rating?
does location affect overall job rating?
Which industry has the best average overall rating?

## Data Source: 
The core question is to determine what features best predicts the over all ratings of a jobs. The initial data comes from the datasets were sourced from Kaggle. the two datasets were merged with 27 columns.

Link to the data set:

https://www.kaggle.com/datasets/davidgauthier/glassdoor-j 
https://www.kaggle.com/datasets/peopledatalabssf/free-7-million-company-dataset

the provisional dataset cleaned and has 11 columns.

(https://github.com/nndavis/final_project/blob/main/data_small.csv)



## Questions hope to answer:
The question we would like to explore is

From running machine learning code, the team hopes to answer the following questions.

what features best predicts the over all ratings of a job

What are the top 3 factors that impact the overall job rating? 

What do future employees look for in a job?



#### Team Communication
We used Slack: for discussion about the project work or troubleshooting

Github Read Me: for project planning and note-taking
        
Zoom: for co-working sessions



## Data Cleaning

The glassdoor reviews data set had originally had 18 columns before we began cleaning the data.
(https://www.kaggle.com/datasets/davidgauthier/glassdoor-job-reviews?resource=download)

For the data cleaning, we used Jupyter Notebook and associated libraries to clean and reformat the data.
After loading the CSV file, we Created a reviews dataframe by dropping columns that are not necessary, then dropping na columns from reviews dataframe. Then we Converted all firms to lowercase string and then Created a new column called name to replace firm.

For the comapnies dataframe we dropped columns that are not necessary, then dropped na columns. 

The companies dataset had originally 11 columns beofre cleaning the data.
(https://www.kaggle.com/datasets/peopledatalabssf/free-7-million-company-dataset)

Then we merged the two datatsets creating a inner join on name column. 

![combined dataset](https://github.com/nndavis/final_project/blob/main/Resources/images/merged_2.png)




## Database
In our analysis there were multiple tables created to help us with visualizations:

we created tables using Postgress SQL. Then we connected our database with AWS cloud console.
companies table image:
 ![Companies table](https://github.com/nndavis/final_project/blob/main/Resources/images/companies_2.png)
 
 
 Reviews table image:
 ![Reviews table](https://github.com/nndavis/final_project/blob/main/Resources/images/review_2.png)
 
 
 combined data table:
  ![combined table](https://github.com/nndavis/final_project/blob/main/Resources/images/merged_2.png)
  
  
  
  ## ERD - Entity Relationship Diagram

Below is an ERD depicting our tables and the relationships between them

<img src="https://raw.githubusercontent.com/nndavis/final_project/Db-AWS/ERD.png">





## Machine Learning

 We used neural networking for our machine learning model. 
The purpose of our model is to classify whether or not a job is good based on a set of features.
Our original dataset of our joined tables contained 29 columns. During the preprocessing step, we dropped down to 11 columns.
Overall_rating is our target. Our features are; name, job title, industry, location, work life balance, culture values,
diversity inclusion, career opportunity, company benefits, and total employee estimate. We chose these features because they are
most applicable when rating a job. 
Those who are looking for a new job, whether they are unemployed or are looking to switch employers, asks about the features we chose to gauge whether they think the job will be a good fit for them. 
Since we are using neural networking, we had to do some encoding on a few features.
These features included; name, job title, industry, and location. This was done by creating a OneHotEncoder instance, 
and then fit and transform the OneHotEncoder using the categorical variable list. After that we added the encoded variable names
back to the dataframe and dropped the originals.
To make our data viable for our deep learning model we used Scikit-Learn to split the data into training and testing sets.
By default, the split is 80% training and 20% testing.
Scikit-Learn was also used to scale the data. The following lines of code are what we did to split and scale:

X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=42)

# Create a StandardScaler instances
scaler = StandardScaler()
![StandardScaler](https://github.com/nndavis/final_project/blob/main/ML_image_Standardscaler_1.png)
![Fit_StandardScaler](https://github.com/nndavis/final_project/blob/main/ML_image_Standardscaler_2.png)

# Fit the StandardScaler
X_scaler = scaler.fit(X_train)

# Scale the data
X_train_scaled = X_scaler.transform(X_train)
X_test_scaled = X_scaler.transform(X_test)

![Train_Test_Accuracy](https://github.com/nndavis/final_project/blob/main/ML_Train_Test_Accuracy%20and%20Loss_results.png)

We chose to use a neural network model because of it's impressive uses when it comes to classification.
A downside to using a neural network is that it is hard to train our data. This may be due to the way our features were encoded.
Another issue is that neural networks have difficulty showing correlation from dependent features to the independent.
The positive to using a neural network is that it uses algorithms that work like a human brain. 
Our data is based off reviews by humans, so it makes sense to use machine learning that mimics those decisions.





#Transfer learning
#SVMs
#XGBoost





## Data Visualization

Tableau Dashboard Link:
[Tableau Dashboard Link]()

The Tableau Dashboard allows users to see 

![Interactive element Image](https://github.com/nndavis/final_project/blob/Tableau/tabeau%20I_E2.png?raw=true)

![Interactive element Image](https://github.com/nndavis/final_project/blob/main/Resources/images/Job%20Ratings%20Dashboard.png)

## Lessons Learned

Future iterations of this analysis could seek the use of:

## Tools
- Jupyter Notebook
- Google Slides
- Tableau
- PgAdmin4
- Github Desktop App
- Microsoft Excel

## Languages & Libraries
- Python
- Pandas
- Postgresql
- Scikit Learn
- TensorFlow
- SqlAlchemy
- Pyscopg2

## Links

- Presentation Link:
[Google Slides Presentation](https://docs.google.com/presentation/d/1GJoxcCFBPjdAIev5j_rdqPTKSKjfAUQVwnmZVa8wTEE/edit?usp=sharing)

- Kaggle Data Sets:
[Kaggle Glassdoor Reviews Dataset](https://www.kaggle.com/datasets/davidgauthier/glassdoor-job-reviews?resource=download) 

[Kaggle companies Dataset ](https://www.kaggle.com/datasets/peopledatalabssf/free-7-million-company-dataset)

- Tableau Dashboard Link:
[Tableau Dashboard Link]()
