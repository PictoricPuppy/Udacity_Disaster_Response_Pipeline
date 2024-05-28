# Udacity_Disaster_Response_Pipeline
Project Disaster Response Pipeline from Udacity Data Science Nanodegree

#**CONTENT**

##**1. Description**
##**2. Files**
##**3. Executing the program**
##**4. Flask web app Overview**

#**1. DESCRIPTION**
Prepare and train a dataset of real messages from natural disasters.
The project is divided in three exercises:
      Reading, formating and cleaning the data with an ETL.
      Build a machine learning pipeline to classify the data.
      Run a flask app to visualize the data in a friendly way.

#**2. FILES**

###Project structure
The project includes an structure of 5 folders.
![image](https://github.com/PictoricPuppy/Udacity_Disaster_Response_Pipeline/assets/116310268/8d5898b5-40d1-4573-b6cb-ddef84476389)

###app  
  Templates > Templates for the flask app
  run.py > Main file to run the app. 

###data
  DisasterResponse.db > Data base with the results of the ETL.
  disaster_categories.csv > Raw data with categories for the messages.
  disaster_messages.csv > Raw data with the recieved messages.
  process_data.py > File to run the ETL. This file loads and cleans the data of 'disaster_messages.csv' and 'disaster_categories.csv'. After processing, it is saved in 'DisasterResponse.db'.

###models
  classifier.pkl > Classifier machine learning model.
  train_classifier.py > Using the cleaned saved in 'DisasterResponse.db' this scrip trains the data set and saves a machine learning model in 'classifier.pkl'.

###root
  README.md > Instructions to complete the flask app and to run the program.

###Jupyter notebook files
  ETL Pipeline Preparation.ipynb > Notebook with the necessary steps to create and prepare the ETL.
  ML Pipeline Preparation.ipynb > Notebook with the necessary steps to create and prepare the ML model.
       
#**3. EXECUTING THE PROGRAM**
   Run the following commands to execute the files and the Flask web app.
   
   ###Create a database.
      python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
       ![image](https://github.com/PictoricPuppy/Udacity_Disaster_Response_Pipeline/assets/116310268/27e40f80-f5a7-44af-9c74-8e2e1b1f04fa)

   ###Create a classifier ML.
      python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
      ![image](https://github.com/PictoricPuppy/Udacity_Disaster_Response_Pipeline/assets/116310268/5d82a4f6-e82f-4df5-a965-2dfe0df7ff76)
      ![image](https://github.com/PictoricPuppy/Udacity_Disaster_Response_Pipeline/assets/116310268/d57fcf34-000c-4dd8-92fc-34213eb794db)

   ###Run the main app.
       python run.py
       ![image](https://github.com/PictoricPuppy/Udacity_Disaster_Response_Pipeline/assets/116310268/cc919d67-3d83-4a97-8d68-1862dfc45bf3)
   
   ###Preview the web app.
       http://0.0.0.0:3000
        ![image](https://github.com/PictoricPuppy/Udacity_Disaster_Response_Pipeline/assets/116310268/518516f5-1fe7-4a18-b2b3-6217cd768bf7)

#**4. FLASK WEB APP OVERVIEW**
   With this flask web app data can be visualized in a easier way and it's easier to test our model.
   
   Message >  'Can't beathe'
   ![image](https://github.com/PictoricPuppy/Udacity_Disaster_Response_Pipeline/assets/116310268/c527aeab-7481-4c95-9c41-eb0c4768e20a)

   Classification outputs
    ![image](https://github.com/PictoricPuppy/Udacity_Disaster_Response_Pipeline/assets/116310268/7a430211-8ce3-4d05-af9b-3cf81b74ba56)
   


   
