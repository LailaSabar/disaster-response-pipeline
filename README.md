# Disaster Response Pipeline Project

In this project, I'll be applying data engineering skills to analyze disaster data from Figure Eight to build a model for an API that classifies disaster messages.

data directory contains a data set which are real messages that were sent during disaster events. I will be creating a machine learning pipeline to categorize these events so that appropriate disaster relief agency can be reached out for help.

This project will include a web app where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data.


## Table of Contents

- [Project Components](#component)
   - [ETL Pipeline](#etl)
   - [ML Pipeline](#ml)
   - [Flask Web App](#flask)
- [Content](#content)
- [Screenshots](#screen)
- [Instructions](#inst)
- [Credits and Acknowledgements](#credits)

***

<a id='component'></a>

## 1. Project Components

There are three components of this project:

<a id='etl'></a>
### 1.1. ETL Pipeline

- Loads the `messages` and `categories` dataset
- Merges the two datasets
- Cleans the data
- Stores it in a SQLite database

<a id='ml'></a>
### 1.2. ML Pipeline

- Loads data from the SQLite database
- Splits the data into training and testing sets
- Builds a text processing and machine learning pipeline
- Trains and tunes a model using GridSearchCV
- Outputs result on the test set
- Exports the final model as a pickle file

<a id='flask'></a>
### 1.3. Flask Web App

- displaying the results in a Flask web app

<a id='content'></a>
## 2. Content
- Data
  - process_data.py: reads in the data, cleans and stores it in a SQL database. Basic usage is python process_data.py MESSAGES_DATA CATEGORIES_DATA NAME_FOR_DATABASE
  - disaster_categories.csv and disaster_messages.csv (dataset)
  - DisasterResponse.db: created database from transformed and cleaned data.
- Models
  - train_classifier.py: includes the code necessary to load data, transform it using natural language processing, run a machine learning model using GridSearchCV and train it. Basic usage is python train_classifier.py DATABASE_DIRECTORY SAVENAME_FOR_MODEL  
- App
  - run.py: Flask app and the user interface used to predict results and display them.
  - templates: folder containing the html templates.

<a id='screen'></a>
## 3. Screenshots

&nbsp;
  &nbsp;
![Drag Racing](images/Capture2.JPG)

&nbsp;

&nbsp;
  &nbsp;
![Drag Racing](images/Capture1.JPG)

&nbsp;

&nbsp;
  &nbsp;
![Drag Racing](images/Capture3.JPG)

&nbsp;

&nbsp;
  &nbsp;
![Drag Racing](images/Capture4.JPG)

&nbsp;

&nbsp;
  &nbsp;
![Drag Racing](images/Capture5.JPG)

&nbsp;

<a id='inst'></a>
## 4. Instructions

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run the web app.
    `python run.py`

3. Now, open another Terminal Window and type : env|grep WORK

4.  In a new web browser window, type in the following: https://SPACEID-3001.SPACEDOMAIN (notice that the SPACEID and SPACEDOMAIN are given by the command in step 3 )

## 5.Credits and Acknowledgements<a name="credits"></a>
Must give credit to Figure Eight for the data.


