# Disaster Response Pipeline Project

### Summary:
This project is motivated by the need for prompt action to be taken for different types of disaster by their respective disaster response organizations. Categorizing disaster related messages can be an aid in this regard.

The final deliverable is Flask app that categorizes input messages into 36 categories with few visualizations.

### Files:

1. `process_data.py`
    - Load the CSV files.
    - Clean the data ( Remove Duplicates ).
    - Save the DataFrame into SQLite db.
    
2. `train_classifier.py`
    - Load and split the data from the SQLite DB into test and train sets.
    - Use GridSearch to find the best parameters of a `RandomForestClassifier`.
    - Save the model as a Pickle file. 

3. `run.py`
    - Run Flask app that classifies disaster related messages to appropiate categories.

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/disaster_message_categories.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/disaster_message_categories.db models/model.p`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
