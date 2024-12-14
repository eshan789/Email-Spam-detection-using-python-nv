About The Project
Spam detection is the process of identifying and filtering out unwanted or unsolicited messages, typically in the form of emails or text messages. These messages are often sent by spammers or malicious actors with the intent of promoting a product, service, or website, or to trick the recipient into providing personal information or downloading malware. Spam detection typically involves the use of machine learning algorithms that can analyze the content of messages and identify patterns or characteristics that are commonly associated with spam. These algorithms can be trained on large datasets of labeled examples of spam and legitimate messages, allowing them to learn to distinguish between the two with a high degree of accuracy. Effective spam detection is an important task for both individuals and organizations, as it can help to prevent unwanted messages from cluttering inboxes, reduce the risk of phishing attacks, and improve overall cybersecurity.

This repository contains a Python script that uses various machine learning models to classify spam messages from ham messages. The model is trained on a Popular dataset of Spam emails and we use multiple machine learning models for classification.

Built With
NumPy

Pandas

Matplotlib

Seaborn

Sklearn


Anyways you can install all the above mentioned libraries at a glance by executing the following command:

pip install -r requirements.txt
Getting Started
This is make you understand how you may give instructions on setting up your project locally. To get a local copy up and running follow these simple example steps.

Installation
Clone the repo

git clone https://github.com/KalyanMurapaka45/Spam-Email-Detection.git
Install the required libraries

 pip install -r requirements.txt
Open and execute .ipynb file (After complete Execution you will get a .pkl file for project Deployment

Dataset Description
We have utilized the Email-Spam dataset, which is publicly available on Kaggle. The dataset comprises a collection of 5,572 emails, each having two features: Category and Message.

Message Message feature contains the actual text of the email.

Category The Category feature distinguishes between Spam and Ham emails

Data Pre-processing
Steps Done:
The Unnamed: 2, Unnamed: 3, and Unnamed: 4 columns are dropped.

The Category column is converted to binary values.

The dataset is split into training and testing sets using train_test_split() function from sklearn.model_selection.

The emails are transformed into numerical features using the TfidfVectorizer() function from sklearn.feature_extraction.text.


Intially the 'Unnamed: 2', 'Unnamed: 3', and 'Unnamed: 4' columns are then dropped from the DataFrame and the code checks for null values in the DataFrame using the 'isnull()' method. The 'Category' column in the DataFrame is then converted to numerical values (0 and 1) where 'spam' is replaced with 0 and 'ham' is replaced with 1. The number of values in each category is printed using the 'value_counts()' method. The X and Y variables are then created where X stores the 'Message' column of the DataFrame, and Y stores the 'Category' column. The code then splits the data into training and testing sets using the 'train_test_split()' method from the scikit-learn library. The TfidfVectorizer is then used to extract features from the text data. The 'min_df' parameter is set to 1, the 'stop_words' parameter is set to 'english', and the 'lowercase' parameter is set to 'True'. The feature extraction is performed on both the training and testing data using the 'fit_transform()' and 'transform()' methods. Finally, the 'Y_train' and 'Y_test' variables are converted to integers.

Model Training and Evaluation
As we already splitted the dataset into training and testing parts, the machine learning models can be able to train on the training data by using fit() method and then we are testing the trained machine learning model by using predict() method. To know the performance of the trained machine learning models we are evaluating the predicted data and original data by using evaluation metrics such as accuracy, precision, recall, and F1-score.

The following Machine Learning Algorithms are used:

Logistic Regression
K Nearest Neighbors
Decision Trees
Random Forest
Stacking model
Model Deployment
The file Spam Classification Deployment.py contains the complete code for deployment which is deployed in Streamlit. Streamlit is an open-source Python library that allows you to create interactive web applications for machine learning and data science projects.

To run the Deployment.py file, Execute the following Command in your command prompt

   python Spam Classification Deployment.py
   ![deployment](https://github.com/user-attachments/assets/ada2e481-fe36-4d26-9a87-47878c93e57c)