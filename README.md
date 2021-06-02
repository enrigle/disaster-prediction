# Disaster Response Pipeline Project

## Code structure

- app
| - template
| |- master.html  # main page of web app
| |- go.html  # classification result page of web app
|- run.py  # Flask file that runs app

- data
|- disaster_categories.csv  # data to process 
|- disaster_messages.csv  # data to process
|- process_data.py # The script takes the file paths of both datasets and database, cleans the datasets, and stores the clean data into a SQLite database in the specified database file path.
|- InsertDatabaseName.db   # database to save clean data to

- models
|- train_classifier.py #Takes the database file path and model file path, creates and trains a classifier, and stores the classifier into a pickle file to the specified model file path
|- classifier.pkl  # saved model 

- README.md



### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `cd app`
    `python run.py`

3. Go to http://0.0.0.0:3001/
# disaster-prediction
# disaster-prediction
