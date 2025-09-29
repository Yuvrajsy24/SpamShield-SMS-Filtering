📩 SMS Spam Classifier using Machine Learning
📚 Overview

This project is a binary classification task that uses various machine learning algorithms to detect whether an SMS message is Spam or Ham (Not Spam). The data comes from the UCI SMS Spam Collection Dataset
, a set of SMS messages tagged as spam or ham.

🗂️ Dataset

File: SMSSpamCollection.txt

Format: Tab-separated values with two columns:

v1: Label (spam or ham)

v2: Message text

Total messages: 5,572

Ham: 4,825

Spam: 747

🔍 Data Preprocessing

Loaded data from Google Drive using pandas.

Renamed columns to v1 (label) and v2 (message).

Added a length column to capture the length of each message.

Removed stop words using sklearn.feature_extraction.text.ENGLISH_STOP_WORDS.

Visualized the data using:

Bar charts

Pie charts

Word frequency plots for both spam and ham messages

🧠 Feature Extraction

Used CountVectorizer to transform text messages into numerical feature vectors:

Shape of feature matrix: (5572, 8675)

Each row = message

Each column = frequency of a word (after stop word removal)

🏷️ Label Encoding

Mapped:

ham → 0

spam → 1

Column added: label_num

🧪 Model Training and Evaluation

Split data:

Training: 67%

Test: 33%

Classifiers Used:
Classifier	Description
SVM	Support Vector Machine
MultinomialNB	Naive Bayes (suitable for text)
GaussianNB	Naive Bayes with Gaussian model
LogisticRegression	Logistic regression
RandomForest	Ensemble of decision trees
AdaBoost	Boosting ensemble method
📈 Evaluation Metrics:

Accuracy

Precision

Recall

F1 Score

🧾 Results:
Classifier	Accuracy (%)	Precision	Recall	F1 Score
SVM	98.91	0.996	0.923	0.958
MultinomialNB	98.04	0.892	0.972	0.930
GaussianNB	90.54	0.593	0.931	0.725
Logistic	98.10	0.961	0.894	0.926
RandomForest	97.77	1.000	0.833	0.909
AdaBoost	92.01	0.867	0.476	0.614

✅ Best performing model: SVM with ~99% accuracy.

🔲 Confusion Matrix for SVM
	Predicted Ham	Predicted Spam
Actual Ham	1592	1
Actual Spam	19	227
📊 Visualization Tools

Word frequency bar charts for spam and ham messages

Pie charts of class distribution

Confusion matrix using pandas and sklearn.metrics

📎 Requirements

Python (≥ 3.6)

Libraries:

pandas

numpy

matplotlib

sklearn

collections

🔌 How to Run

Upload SMSSpamCollection.txt to your Google Drive.

Use Google Colab and run the notebook.

Mount your Drive to access the file.

Run each cell step-by-step for preprocessing, training, and evaluation.

🧾 License

This project is for educational purposes only. Dataset originally published by UCI Machine Learning Repository.
