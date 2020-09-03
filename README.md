# Disaster Response Pipelines Project

# Project Description
In this project, we will build a model to classify messages that are sent during disasters. There are 36 pre-defined categories, and examples of these categories include Aid Related, Medical Help, Search And Rescue, etc. By classifying these messages, we can allow these messages to be sent to the appropriate disaster relief agency. This project will involve the building of a basic ETL and Machine Learning pipeline to facilitate the task. This is also a multi-label classification task, since a message can belong to one or more categories. We will be working with a data set provided by [Figure Eight](https://www.figure-eight.com/) containing real messages that were sent during disaster events.

Finally, this project contains a web app where you can input a message and get classification results.

![Screenshot of Web App](Screenshot_2.PNG)

## Files Structure
~~~~~~~
	disaster_response_pipeline
		│   README.md
		│   Screenshot_1.png
		│   Screenshot_2.png
		│
		├───app
		│   │   run.py
		│   │
		│   └───templates
		│           go.html
		│           master.html
		│
		├───data
		│       DisasterResponse.db
		│       disaster_categories.csv
		│       disaster_messages.csv
		│       process_data.py
		│
		├───data_prep
		│   │   DisasterResponse.db
		│   │   ETL Pipeline Preparation.ipynb
		│   │   ML Pipeline Preparation.ipynb
		│   │
		│   └───data
		│           categories.csv
		│           DisasterResponse.db
		│           messages.csv
		│
		└───models
				Classifier.pkl
				train_classifier.py
~~~~~~~
## Installation

This project requires Python 3.x and the following Python libraries:

* Machine Learning Libraries: NumPy, SciPy, Pandas, Sciki-Learn
* Natural Language Process Libraries: NLTK
* SQLlite Database Libraqries: SQLalchemy
* Web App and Data Visualization: Flask, Plotly

## File Descriptions
1. App folder including the templates folder and "run.py" for the web application
2. Data folder containing "DisasterResponse.db", "disaster_categories.csv", "disaster_messages.csv" and "process_data.py" for data cleaning and transfering.
3. Models folder including "Classifier.pkl" and "train_classifier.py" for the Machine Learning model.
4. README file
5. data_prep folder containing 6 different files, which were used for the project building. (Please note: this folder is not necessary for this project to run.)


## Instructions
1. Clone this repository

```
git clone https://github.com/msobrinoestevez/Disaster-response-pipelines
```

2. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/Classifier.pkl`

3. Run the following command in the app's directory to run your web app.
    `python run.py`

4. Go to http://0.0.0.0:3001/


## Example

1. Input: we need help to overcome the coronavirus. masks, doctors, nurses. We need water and military protection
2. Predicted classes:
![Screenshot of Predicted Classes](Screenshot_1.PNG)
