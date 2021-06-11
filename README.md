# Disaster Response Pipeline Project

## 1. Project Description
This Project is part of Data Science Nanodegree Program by Udacity in collaboration with [Figure Eight](https://www.figure-eight.com/)<br/>
The initial dataset contains pre-labelled tweet and messages from real-life disaster. 
The aim of the project is to build building of a basic ETL (Extract Transform & Load) and Natural Language Processing and Machine Learning pipeline to facilitate the task. This is also a multi-label classification task, since a message can belong to one or more categories.<br/>
There are 36 pre-defined categories, and examples of these categories include Aid Related, Medical Help, Search And Rescue, etc. By classifying these messages, we can allow these messages to be sent to the appropriate disaster relief agency.<br/>

Finally, this project contains a web app where you can input a message and get the classification results.

![Screenshot of Web App](WebApp.PNG)

## 2. Repository Structure
~~~~~~~
        Disaster-Response
          |-- app
                |-- templates
                        |-- go.html # classification result page of web app
                        |-- master.html # main page of web app
                |-- run.py # Flask file that runs app
          |-- data
                |-- disaster_message.csv # data to process
                |-- disaster_categories.csv # data to process
                |-- DisasterResponse.db # database to save clean data to
                |-- process_data.py
          |-- models
                |-- classifier.pkl # saved model
                |-- train_classifier.py
          |-- Prep # contains jupyter notebooks
                |-- categories.csv
                |-- ETL Pipeline Preparation.ipynb
                |-- ETL_Preparation.db
                |-- messages.csv
                |-- ML Pipeline Preparation.ipynb
          |-- README
~~~~~~~

## 3. Installation
The required libraries for running the code within Jupiter notebook & python files are part of the Anaconda distribution for Python 3.6.7. Following libraries were used:

* numpy
* pandas
* sqlalchemy
* re
* NLTK
* pickle
* sklearn
* plotly
* flask

## 4. Project Motivation
Disasters call for medical emergency, food, medicines, etc.<br/>
This flask app is used to classify messages that are sent by twitter users during disasters requesting help. We then can let government agencies know what the most immediate need at a particular area is.

## 5. Files Description
1. **app** folder including the **templates** folder and `"run.py"` for the web application. "`run.py`" is main file to run the app.

2. **data** folder contains:
* "`disaster_messages.csv`" containing the messages which are sent during the disaster.
* "`disaster_categories.csv`" containing data about the categories of the disasters.
* "`DisasterResponse.db`" which is the database created after cleaning the data i.e. contains clean data.
* "`process_data.py`" contains the code in python file for data cleaning, transforming and save it into a new database called `DisasterResponse.db`.

3. **models** folder contains:
* "`classifier.pkl`" which is the model we build.
* "`train_classifier.py`" contains code in python file for training the Machine Learning model.

4. **Preparation** folder contains different jupyter notebook files which were used for the project building. (**`Please note:`** `this folder is not necessary for this project to run`.)<br/>
Files are:
* `"categories.csv"` same file as "`disaster_categories.csv`".
* `"messages.csv"` same file as "`disaster_messages.csv`".
* `"ETL Pipeline Preparation.ipynb"` contains code for data cleaning & preparation in jupyter notebook.
* `"ETL_Preparation.db"` same as `"DisasterResponse.db"`.
* `"ML Pipeline Preparation.ipynb"` contains code for preparing ML Pipeline & model in jupyter notebook.

## 6. Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database <br/>
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves <br/>
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

## 7. Additional Material:
In the **data** and **models** folder you can find two jupyter notebook that will help you understand how the model works step by step:
1. **ETL Preparation Notebook**: learn everything about the implemented ETL pipeline
2. **ML Pipeline Preparation Notebook**: look at the Machine Learning Pipeline developed with NLTK and Scikit-Learn

You can use **ML Pipeline Preparation Notebook** to re-train the model or tune it through a dedicated Grid Search section.
In this case, it is warmly recommended to use a Linux machine to run Grid Search, especially if you are going to try a large combination of parameters.
Using a standard desktop/laptop (4 CPUs, RAM 8Gb or above) it may take several hours to complete. 

<a name="authors"></a>
## 8. Authors

* [Chakradhaar Viswatmula](https://github.com/chakradhaarrv)

## 9. Acknowledgements

* [Udacity](https://www.udacity.com/) for providing such a complete Data Science Nanodegree Program
* [Figure Eight](https://www.figure-eight.com/) for providing messages dataset to train my model