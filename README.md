# UCBerkeley_MLAI_PracticalApplication02 - Practical Application III: Comparing Classifiers

**Overview**: In this practical application, your goal is to compare the performance of the classifiers we encountered in this section, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines.  We will utilize a dataset related to marketing bank products over the telephone.  

### Getting Started

Our dataset comes from the UCI Machine Learning repository [link](https://archive.ics.uci.edu/ml/datasets/bank+marketing).  The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns.  We will make use of the article accompanying the dataset [here](CRISP-DM-BANK.pdf) for more information on the data and features.

##### Python File  : https://github.com/githubgscoder/UCBerkeley_MLAI_PracticalApplication03/blob/main/prompt_III.ipynb
##### Datafile     : https://archive.ics.uci.edu/ml/datasets/bank+marketing
##### GitHub Link  : https://github.com/githubgscoder/UCBerkeley_MLAI_PracticalApplication03.git

### Data Cleaning and Preparation:
1. Read the file and reviewed the data
2. Decided to keep all features and mapped target column 'y' to convert 'yes' as 1 and 'no' as 0.
3. Data has no null values

### Business Objective
To predict whether or not a person will subscribe to a term deposit that would help target potential clients based on their characteristics and previous interaactions with the bank.

### Preprocessing Data
1. Grouped features into categorical and numerical based on the data types.
2. Created a preprocessor with ColumTransformer to encode all the numerical values with StandardScaler() and all the categorical columns with OneHotEncoder()
3. Split the test and train data with a test size of 30%
4. Calculated baseline accuracy at 62.105%

### Simple Model and it's Train and Test Accuracy
1. Created a pipeline to preproccess the data and applly a LogisticReggression() classifier
2. Train accuracy: 0.912, Test accuracy: 0.912

### Model Comparisons
![image](https://github.com/user-attachments/assets/99f3f0fa-a195-4c86-8255-9e9db8ba30ed)

Visualizations
  - Train time for different models
    
    ![image](https://github.com/user-attachments/assets/26454301-6152-4638-a2a3-1233bcabaaec)

  - Train and test Accuracy for different models

    ![image](https://github.com/user-attachments/assets/7d0d93b9-a948-47f8-b6af-bc103ccee145)

  - Train time vs Train Accuracy

    ![image](https://github.com/user-attachments/assets/f3b9c9ed-edc0-4db8-8471-c3c46ab4affa)

### Feature Engineering, Hyperparameter tuning with GridSearch
1. Added an additional feature by creating bing to group folks into particular age groups '<25', '25-35', '35-45', '45-55', '55-65', '65+'
2. Removed the age column and preprocessed the dataset again
3. Added additional parameter for hyperparameter tuning
4. Performed GridSearch
5. Created a dataframe to capture the,
   a. Model
   b. Best Paramters
   c. Train Accuracy
   d. Test Accuracy
   e. F1 Score
   f. ROC AUC Score
   
   ![image](https://github.com/user-attachments/assets/5e4c7d9d-f5b6-468d-9095-9de5f71272da)
   Note: attached file to the repository as results_df

#### Model Performance Metrics
  ![image](https://github.com/user-attachments/assets/3cd5ead2-e7bd-4fd7-8b73-e16bb247eac6)


     




#### Additional Visualizations of the campaign dataframe
1. Target Variable - [Skewed towards "No"]

   ![image](https://github.com/user-attachments/assets/c1f5c0a7-1f9b-46d1-ad06-7b19c3541fdc)

2. Box Plot of age by subscription to term deposit

   ![image](https://github.com/user-attachments/assets/cfeb09f4-9a7b-44e6-8c40-cf1e214d65cf)

3. Duration by subscriptions to term deposit

   ![image](https://github.com/user-attachments/assets/3403b1ef-e4c4-4f40-b135-9c516f499fee)

4. Plot of continous variables from the dataset

   ![image](https://github.com/user-attachments/assets/25468076-8b8d-4e5b-9f02-8228bea30f00)



