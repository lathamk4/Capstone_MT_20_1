Dataset & reference: https://www.kaggle.com/datasets/tboyle10/medicaltranscriptions

# Goal:
The goal of this project is to build a machine learning model that can accurately predict the medical specialty based on the content of medical transcriptions. 
This will help automate classification, streamline healthcare workflows, and support faster and more accurate specialist referrals.
Few Classifier Models under consideration:
1)Logistic Regression 
2)Multinomial Naive Bayes
3)Support Vector Machine (SVM)
4)Random Forest 
5)Transformer-based models (e.g., BERT)

# Business Objective: 
The objective is to automate classification of medical specialties from transcriptions to streamline clinical workflows. This enhances care coordination by routing information to the correct specialists. 
It also supports efficient resource allocation and operational planning. Ultimately, it improves patient outcomes and reduces administrative burden.

# Exploratory Data Analysis: 
As part of the data analysis following operations were performed 

#1) Data Cleaning: 
For this project, we are considering only the transcription column and medical speciatly as the traget label columns. Hence dropping all other columns. 
There are 33 null values in the Specialty column which is filled with 'unknown' . 

#2)Text Preprocessing:
Lowercasing , Removing Punctuation and Stop words were used. Tokenization and Lemmatization has to be implemented but Punkt is not downloding properly. Working on fixing the errors. 

#3) Data Visualization: 
a) Distribution of medical specialty: 
This plot helps find any imbalance in the dataset and based on the observation we can use techniques like oversampling or undersampling to overcome the bias or variance
b) Trasncription length by Medical specialty: 
This plot helps identify which specialties produce longer or more detailed notes, guiding preprocessing and model input length. It also reveals content variability, useful for customizing NLP models per specialty.
c) TOP TF-IDF terms by medical specialty plot :
d) Top 10 most common words per Medical specialty plot:
Both the plot helps identifying unique words specific to specialty thereby enhacing the feature extraction and specialty specific text classification
e) word cloud by transcriptions : 
This plot helps visualize most frequent terms among all the specialities and aids in the quick exploratory analysis 
f) Top 10 Most frequent word specific to specialty 
This plot helps with identifying the specialty-specific language pattern which in turn improve model performance.

#4) Feature Engineering : 
Identifying and extract terms specific to the medical specialty using the clinical BERT 
Identify the NER to extract entities like patient age and sex and remove from transcriptions.

#5 Initial Modeling:
The Multinomial Naive Bayes classifier model is used for training and Accuracy score was just 37%. 
More to explore and fine tune in the next module . 
