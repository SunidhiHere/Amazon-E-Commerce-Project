# Amazon-E-Commerce-Project
<img width="1408" height="484" alt="Gemini_Generated_Image_btb3uabtb3uabtb3" src="https://github.com/user-attachments/assets/afef8efa-af6c-473a-ba97-eb602017cad2" />


## Introduction
The rapid growth of e-commerce platforms has generated massive amounts of customer review data, making it difficult for businesses to manually analyze customer opinions and feedback. This project focuses on applying Natural Language Processing (NLP) techniques to Amazon product reviews in order to extract meaningful insights from unstructured text data.
The main objective of this project is to analyze customer sentiments, identify common product-related issues, and understand customer preferences using machine learning and NLP methods. By processing and interpreting review text, the project helps simulate how companies like Amazon can improve customer experience, enhance product quality, and make data-driven business decisions.
The project includes various stages of the NLP pipeline such as text preprocessing, tokenization, stopword removal, stemming/lemmatization, feature extraction, and sentiment analysis. Different visualization and analytical techniques are also used to better understand customer behavior and review patterns.
This project demonstrates practical applications of NLP in the e-commerce domain and showcases skills in data cleaning, text analytics, machine learning, and business insight generation using real-world customer review data.

## About Dataset 
The dataset used in this project contains Amazon customer reviews and product-related information collected from the Amazon e-commerce platform. It is mainly used for Natural Language Processing (NLP) tasks such as sentiment analysis, customer opinion mining, and review classification. The dataset includes textual reviews, ratings, and other product/customer details that help in understanding customer behavior and product performance.
## Project Pipeline
Business Problem Understanding
Data Collection & Loading
Data Cleaning & Preprocessing
Missing Value Treatment
Data Type Conversion
Exploratory Data Analysis (EDA)
Churn Pattern Analysis
Feature Engineering & Encoding
Feature Scaling & Selection
Train-Test Split
Model Building (Logistic Regression, Decision Tree, Random Forest, SVM)
Model Evaluation & Comparison
Confusion Matrix Analysis
Feature Importance Analysis
Business Insights Generation
Customer Retention Recommendations

## EDA
The analysis was performed on an Amazon product sales dataset containing product details, pricing information, ratings, reviews, and category data.

Key Findings
Product Categories
The dataset is dominated by Electronics, Computer Accessories, and Home & Kitchen products.
Most products are related to electronic devices and accessories.
Pricing Analysis
Both actual and discounted prices are positively skewed, indicating that most products are relatively low-priced while a few premium products have very high prices.
The majority of products receive discounts between 50% and 70%.
Electronics products show the largest price reductions after discounts.
Most products have an actual price below ₹20,000, while discounted prices are generally below ₹10,000.
Ratings Analysis
Most product ratings fall between 4.0 and 4.5, indicating generally positive customer feedback.
No products have ratings below 2.0.
The majority of products are classified as Above Average based on rating categories.
Products in categories such as Toys & Games, Health & Personal Care, and Car & Motorbike maintain consistently high ratings.
Review Analysis
Review counts are highly skewed, with a small number of products receiving extremely large numbers of reviews.
Several users have reviewed multiple products, while many reviews are posted under generic names such as "Amazon Customer."
Correlation Analysis
A strong positive relationship exists between actual price and discounted price.
Other numerical features show relatively weak correlations.
Overall Insight

The dataset reveals that Amazon's marketplace is heavily driven by electronics-related products, with substantial discounts playing a major role in pricing strategy. Customer ratings are generally high across categories, indicating strong user satisfaction, while product popularity varies significantly based on review volume and category.

## Model
## Machine Learning & Sentiment Analysis Summary

This project incorporates both predictive modeling and natural language processing (NLP) techniques to analyze product characteristics and user review patterns.

### 1. Sentiment Analysis (NLP)
* **Algorithm/Library:** VADER (Valued Sentiment Dictionary and Sentiment Reasoner) via `nltk.sentiment.vader.SentimentIntensityAnalyzer`.
* **Objective:** To evaluate and quantify the textual content of user reviews (`review_content`) into standard sentiment metrics.
* **Outputs:** For each product review, the algorithm calculates:
  * **Positive Score**
  * **Neutral Score**
  * **Negative Score**
  * **Compound Score** (A normalized metric bridging `-1` for extreme negative sentiment and `+1` for extreme positive sentiment).
* **Usage:** Used to establish data-driven trends between buyers' written sentiment scores and their corresponding numerical star ratings.

### 2. Predictive Modeling & Statistical Diagnostics
* **Algorithm:** Ordinary Least Squares (OLS) Linear Regression.
* **Objective:** To test linear relationships between numerical features (such as pricing metrics and review trends).
* **Statistical Insights & Validations:**
  * **Residual Analysis:** A residual plotting stage was integrated to validate key regression assumptions.
  * **Heteroscedasticity Assessment:** Diagnostic plots revealed the presence of *Heteroscedasticity* (non-constant variance in error terms across the predictor range). 
  * **Conclusion:** Because the assumption of homoscedasticity was violated, the notebook establishes that the baseline data requirements for a reliable Linear Regression model are **not met**, underscoring the necessity for alternative non-linear models or transformation pipelines in future iterations.

## Model Evaluation
