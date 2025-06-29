# Book Popularity Prediction

This project aims to build a machine learning model that predicts whether a book will be popular based on a variety of features extracted from book metadata and user reviews.

## Objective

To classify books as **popular** or **not popular** using both structured data (e.g., price, categories) and unstructured data (e.g., review text, summary, and description).

## Dataset

The dataset includes the following features:

* `price`
* `popularity` (target variable)
* `review/summary`
* `review/text`
* `review/helpfulness`
* `authors`
* `categories`
* `description`

## Data Preprocessing

* Filtered book categories with at least 100 instances
* Converted categorical variables to dummy/indicator variables
* Parsed `review/helpfulness` into:

  * `num_review`
  * `num_helpful`
  * `perc_helpful_reviews`
* Normalized text fields to lowercase

## Text Feature Engineering

Extracted signals from unstructured text using a bag-of-words model based on a predefined list of positive sentiment words (e.g., "great", "amazing", "fantastic", etc.). Applied `CountVectorizer` to:

* `review/text`
* `review/summary`
* `description`

## Modeling

The model-building section follows the preprocessing. If available, include:

* Model type used (e.g., Logistic Regression, Random Forest, etc.)
* Performance metrics (accuracy, F1 score, confusion matrix)
* Cross-validation or test/train split strategy


## Future Work

* Use TF-IDF or transformer-based embeddings for richer text features
* Add model comparison (Logistic Regression vs. Random Forest vs. XGBoost)
* Hyperparameter tuning and pipeline optimization

---

Let me know if you want this saved as a `.md` file or need further customization.
