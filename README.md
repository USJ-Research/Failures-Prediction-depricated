# AI-Driven Predictive Failure Detection for Kubernetes Deployments

This repository contains a machine learning experiment for detecting server errors in Kubernetes application logs.

## Dataset

- 13,300 log records
- 89 unique log patterns
- Fields: event, HTTP method, request path, and status code
- Binary labels based on HTTP status:
  - `0`: Normal or non-server-error
  - `1`: Server error (500+)

## Implementation

The repository includes a Google Colab notebook that:

- Cleans and explores the dataset
- Combines log fields into text features
- Uses TF-IDF for feature extraction
- Trains a balanced Random Forest classifier
- Evaluates performance using accuracy and classification metrics
- Tests predictions on new log entries
- Exports the trained model as a `.pkl` file

## Current Result

The Random Forest model achieved 100% accuracy on a random 80/20 stratified test split. This result requires further validation on unseen patterns and real-world logs.

## Technologies

Python, Pandas, Scikit-learn, XGBoost, Matplotlib, Joblib, Jupyter, and Google Colab.

## Future Work

- Validate performance on unseen log patterns
- Improve dataset diversity
- Compare multiple ML algorithms
- Add Prometheus and Loki log collection
- Support continue, pause, and rollback decisions
