# indeed-salary-prediction-nlp
Salary prediction from Indeed job postings using NLP and Machine Learning (group project, ISDS 2021)

# Salary Prediction from Indeed Job Postings using NLP and Machine Learning

## Overview
Group project for Introduction to Social Data Science (University of Copenhagen, 
Summer 2021). The project scrapes job postings from Indeed.com and predicts 
whether a job's salary is above or below the median, using text data from job 
titles and descriptions.

## Data
- Source: Indeed.com, scraped using BeautifulSoup
- Scope: Economics-related job postings in the United States
- Initial dataset: 1,419 job postings
- After cleaning (postings with salary information): 359 observations

## Methodology
- Web scraping with BeautifulSoup, including rate-limiting and adherence to 
  data ethics principles (Salganik, 2017)
- Text cleaning and preprocessing with NLTK (stopword removal, tokenization, 
  lemmatization)
- Models: Logistic Regression, LASSO, Random Forest (salary above/below 
  median classification), Bernoulli Naive Bayes (high-salary keyword prediction)

## Results

| Model         | Data      | Train Accuracy | Test Accuracy |
|---------------|-----------|-----------------|-----------------|
| Random Forest | Job Title | 77.1%           | 70%             |
| Random Forest | Summary   | 94.1%           | 65%             |

The gap between train and test accuracy indicates some overfitting, 
particularly on the summary data — discussed further in the full report.

## Note
This was a group project completed as part of a university course.

## Tools & Libraries
Python, BeautifulSoup, NLTK, scikit-learn, pandas, matplotlib, seaborn, WordCloud

## Full Report
See `indeed_salary_prediction_report.pdf` for the complete written analysis, 
including the data ethics discussion and limitations.
