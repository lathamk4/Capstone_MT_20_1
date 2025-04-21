Link to the solution: https://github.com/lathamk4/Capstone_MT_20_1/blob/main/Capstone.ipynb

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
![1](https://github.com/user-attachments/assets/26947e16-48e1-4606-bcc8-9dd9e38bb9ed)

b) Trasncription length by Medical specialty: 
This plot helps identify which specialties produce longer or more detailed notes, guiding preprocessing and model input length. It also reveals content variability, useful for customizing NLP models per specialty.
![2](https://github.com/user-attachments/assets/21427796-18b2-4c34-9efe-c3d078654c7b)
c) TOP TF-IDF terms by medical specialty plot :
![3](https://github.com/user-attachments/assets/f47ee9ea-5f73-433d-84c9-5220f262a57f)

d) Top 10 most common words per Medical specialty plot:
![4](https://github.com/user-attachments/assets/c3594832-0fb4-4b4a-b016-8e92f55bb828)

Both the plot helps identifying unique words specific to specialty thereby enhacing the feature extraction and specialty specific text classification
e) word cloud by transcriptions : 
![5](https://github.com/user-attachments/assets/9362656c-d89c-49e8-ac90-d35e78af249c)

This plot helps visualize most frequent terms among all the specialities and aids in the quick exploratory analysis 
f) Top 10 Most frequent word specific to specialty 
![6](https://github.com/user-attachments/assets/3153c211-6db4-41fa-97e8-c99e11c7cb65)

This plot helps with identifying the specialty-specific language pattern which in turn improve model performance.

#4) Feature Engineering : 
Identifying and extract terms specific to the medical specialty using the clinical BERT 
Identify the NER to extract entities like patient age and sex and remove from transcriptions.

#5 Initial Modeling:
The Multinomial Naive Bayes classifier model is used for training and Accuracy score was just 37%. 
More to explore and fine tune in the next module . 
