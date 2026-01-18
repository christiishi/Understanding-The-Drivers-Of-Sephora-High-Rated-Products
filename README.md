# Sephora Product & Review Analysis: Understanding Drivers of High-Rated Products
This project analyzes Sephora product and review data to identify the key factors that drive high product ratings. Using supervised machine learning models, the analysis examines how product attributes, brand identity, pricing, and review volume influence the likelihood of a product receiving a high rating. The results provide actionable insights to support merchandising, marketing strategy, and customer trust initiatives.

## Problem Statement
Beauty retailers face the challenge of promoting the right products while maintaining customer trust in ratings and reviews. Product ratings are influenced by a mix of brand reputation, customer engagement, and review volume, making it difficult to distinguish truly high-performing products from those benefiting from popularity bias.
This project aims to:
* Identify brands that consistently produce highly rated products
* Understand how the number of reviews impacts rating probability
* Determine which product attributes most strongly predict high ratings
* Provide data-driven recommendations to support merchandising and marketing decisions

## Data
**Source**: Kaggle – Sephora Products and Skincare Reviews dataset

**Product Data**: ~8,000 beauty products

**Review Data**: ~1 million user reviews across ~2,000 skincare products

**Final Dataset Size**:
* Product Data: 4,710 rows
* Review Data: 1,092,967 rows

**Key Features**:
* Brand, price, size, and ingredients
* Product categories (primary, secondary, tertiary)
* Review count and rating
* Product flags (Sephora exclusive, new product)

## Data Processing 
* Removed rows with missing reviews and incomplete product attributes
* Reset indices and validated data integrity across product and review datasets
* Visualized categorical distributions to understand feature balance
* Applied one-hot encoding to categorical variables
* Split data into 80% training and 20% testing sets for modeling

## Modeling Approach 
**High-Rating Prediction (Supervised Learning)**
* Built Logistic Regression models to estimate the probability of a product receiving a high rating
* Addressed class imbalance in rating outcomes by applying SMOTE (Synthetic Minority Over-sampling Technique) to improve minority class representation and model reliability.
* Evaluated performance using accuracy, ROC-AUC, precision, recall, and F1-score
* Analyzed model coefficients to interpret brand and feature influence

**Feature Importance**
* Implemented a Random Forest classifier to capture non-linear relationships
* Compared performance against logistic regression
* Extracted feature importance scores to identify the strongest rating drivers, including review count, price, and product category

## Key Results & Insights
* Certain brands consistently demonstrated significantly higher predicted probabilities of receiving high ratings
* Number of reviews emerged as the strongest predictor of high ratings, highlighting the importance of customer engagement
* Products with very few reviews showed unstable rating probabilities, while moderately reviewed products achieved higher and more consistent ratings
* Random Forest models outperformed logistic regression in capturing complex feature interactions, achieving approximately 93% accuracy

## Business Recommendations
Based on our analysis, we recommend the following actions to improve product promotion and customer trust:
* Prioritize high-performing brands in merchandising and marketing
  * Feature brands with consistently high predicted rating probabilities more prominently in homepage placements, curated collections (e.g., “Best of Skincare”), and email or app-based campaigns.
* Actively encourage customer review generation
  * Increase review volume for under-reviewed products through post-purchase incentives, early-access programs, and structured review prompts to improve rating reliability and visibility.

These strategies allow Sephora to better allocate marketing resources, elevate trustworthy brands, and reduce uncertainty in merchandising decisions.
 
## Limitations
* Ratings are heavily skewed toward the 4–5 range, which impacts model balance
* One-hot encoding resulted in high-dimensional feature space, reducing interpretability
* Most products fall within the 0–10 review range, limiting confidence in rating predictions for low-volume items
* Product ratings may reflect brand perception rather than objective product quality

## My Contributions
* Led the development of Random Forest classification models to capture non-linear relationships between product attributes, review volume, and rating outcomes
* Created and analyzed model-driven visualizations to evaluate feature importance and predictive behavior
* Translated technical findings into actionable business recommendations aligned with marketing and merchandising objectives

## Contributors 
* **Christie Shin**
* Shivani Vallamdas
* Vishal Srivastava
* Shuai Zhao
* Gema Zhu
