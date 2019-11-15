A project that uses data engineering skills to analyze disaster data from Figure Eight to build a model for an API that classifies disaster messages. The project is a part of Udacity's Data Scientist nanodegree.

Project Components and Stages
There are three components for this project in two stages.

The components are:

ETL Pipeline
ML Pipeline
Flask Web App
Stage 1. Through Jupyter notebooks
This stage includes working with two jupyter notebook files:

ETL Pipeline Preparation.ipynb which is used to read, clean, and reload the data both in normal way and through pipelines.
ML Pipeline Preparation.ipynb which is used to construct a ML algorithm to predict the keywords from messages. The operation also includes both in normal way and through pipelines.
Stage 2. Updating the web app files
In tHis stage, we moved the final code from the jupyter notebooks to the following .py files:

Stage2\data\process_data.py for reading, cleaning, and reloading the data to SQL db.
The original data is in disaster_categories.csv and disaster_messages.csv files, and the output file is DisasterResponse.db

Stage2\models\train_classifier.py
The code reads the db file then exports the trained model to classifier.pkl file.

Stage2\app\run.py which run the web app.
Instructions To build the model and the database:
Run the following commands in the project's root directory to set up your database and model.

To run ETL pipeline that cleans data and stores in database python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
To run ML pipeline that trains classifier and saves python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
Run the following command in the app's directory to run your web app. python run.py

Go to http://0.0.0.0:3001/ (See below for instructions)
