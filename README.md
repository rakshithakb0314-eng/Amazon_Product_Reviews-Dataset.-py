# Amazon_Product_Reviews-Dataset.-py
Project Overview
This project performs Sentiment Analysis on textual data such as customer reviews, tweets, or comments using Natural Language Processing (NLP) and a pre-trained DistilBERT model from the Hugging Face Transformers library.
The model classifies text into:
POSITIVE
NEGATIVE
The project demonstrates:
Data preprocessing
Sentiment prediction using a Transformer model
Performance evaluation
Data visualization
Insight generation
Features
Cleans and preprocesses text data.
Uses a pre-trained DistilBERT sentiment analysis model.
Predicts sentiment labels and confidence scores.
Evaluates model performance using:
Classification Report
Confusion Matrix
Visualizes results with Seaborn and Matplotlib.
Exports sentiment predictions to a CSV file.
Technologies Used
Python
Pandas
Matplotlib
Seaborn
Hugging Face Transformers
Scikit-learn
Regular Expressions (Regex)
Dataset Requirements
The dataset must be in CSV format and contain the following columns:
Column
Description
text
Input text (reviews, tweets, comments, etc.)
label
Actual sentiment label (POSITIVE/NEGATIVE)
Example Dataset
text
label
This product is amazing!
POSITIVE
Worst experience ever.
NEGATIVE
Excellent quality and service.
POSITIVE
Very disappointing purchase.
NEGATIVE
Installation
Install the required libraries:
Bash
pip install pandas matplotlib seaborn scikit-learn transformers torch
Project Workflow
1. Load Dataset
The dataset is loaded using Pandas.
Python
df = pd.read_csv("reviews.csv")
2. Text Preprocessing
The preprocessing function:
Removes URLs
Removes mentions (@username)
Removes hashtags
Removes special characters
Converts text to lowercase
Example:
Input:
Plain text
@user Amazing product! #happy https://example.com
Output:
Plain text
amazing product
3. Sentiment Prediction
The project uses:
Python
distilbert-base-uncased-finetuned-sst-2-english
This model is fine-tuned for binary sentiment classification.
Example output:
Plain text
Text: amazing product...
Sentiment: POSITIVE
Score: 0.99
4. Model Evaluation
Performance is measured using:
Classification Report
Provides:
Accuracy
Precision
Recall
F1-Score
Confusion Matrix
Visualizes:
True Positives
True Negatives
False Positives
False Negatives
5. Insights Generation
The notebook displays:
Sentiment Distribution
Example:
Plain text
POSITIVE    72%
NEGATIVE    28%
Most Positive Reviews
Shows reviews with highest confidence scores.
Most Negative Reviews
Shows highly confident negative predictions.
6. Save Results
Predictions are saved to:
Plain text
sentiment_results.csv
Output columns:
Column
text
label
clean_text
predicted_sentiment
predicted_score
Expected Output
Sample Prediction
Plain text
Text: this phone is fantastic
Sentiment: POSITIVE
Score: 0.998
Confusion Matrix
A heatmap showing prediction performance.
Sentiment Distribution
Plain text
POSITIVE    75%
NEGATIVE    25%
Folder Structure
Plain text
Sentiment-Analysis-Project/
│
├── reviews.csv
├── sentiment_analysis.ipynb
├── sentiment_results.csv
├── README.md
└── requirements.txt
Applications
Product Review Analysis
Customer Feedback Monitoring
Social Media Sentiment Tracking
Brand Reputation Analysis
Market Research
Opinion Mining
Conclusion
This project leverages the power of DistilBERT, a lightweight Transformer model, to perform accurate sentiment analysis on textual data. It provides an end-to-end workflow from data preprocessing to model evaluation and insight generation, making it suitable for academic projects, internships, and real-world NLP applications.
