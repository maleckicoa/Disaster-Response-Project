# Disaster Response Project

### Table of Contents

1. [Installation](#installation)
2. [Motivation](#motivation)
3. [Files](#files)
4. [Results](#results)
5. [Licensing](#licensing)

## Installation <a name="installation"></a>
The scripts should be run in linux terminal. 
Only one .ipynb script which is provided for experimentation should be run in jupyter notebook

## Motivation <a name="Motivation"></a>
This Project is a classification engine that can be used to processes social text messages in times of disaster. 
The algorithm classifies text messages into more than 30 different categories based on their content.
Each category represents a type of help/support which needs to be provided in times of disaster.
The goal is to be able to quickly respond to a large amount of text messages and provide adequate help.

## Files
1- Attached are two .csv files which contain the messages which are labeled into 36 different categries. 

2- There is also the "Code and Files.zip" file which contains the following files and folders:

    folder "data"       - contains the "process_data.py" script which cleans the data
    folder "models"     - holds the "train_classifier.py" script which transform the text data and applies a classification model.
    folder "app"        - holds the "run.py" script which prepares data for the visualisation, and also the "go.html" and "master.html" which provide the *visualisation and the *app in the browser (see Results)
    
    file "classifier.pkl"       - this is the output of the "train_classifier.py" script. It is the model saved with trained parameters.
    file "DisasterResponse.db" - this is the output of the "process_data.py" script. It is cleaned data now stored in a data base.
    
3- NLP-Disaster.ipynb script contains various models whose perfomance was tested

## Results
The End result of the Project is a Web App which takes text messages as input, and outputs the category/categories which are corresponding to the message content. Ideally, this output should summarize the essence of the message.

The model used was Random Forest Classification. 
Please note that I have faced time issues when training the model. Therefore the model was finaly trained on around 3K observations, although the data set hold 25K+ observations. Also I have applied the Grid Search in order to find the best parameters for the model, but due to time issues only some parameter values could be tested. I strongly encourage anyone who might have adequate processing power and would like to continue working on this project, to train the model on the whole training set and also to include more parameters in the Grid Search.

The overall perfomance was low with about 55% in Averaged Balanced Accuracy 
(This is the average accuracy score across 35 categories; Note that Accuracy used was Balanced Accuracy, because the data set is havily unbalanced). 
However other algorithms might show better performance, but are harder to train. (e.g. SVM model showed 64% Average balanced Accuracy). 
For an overview of models which were used for experimentation please take a look at the the NLP-Disaster.ipynb file


To run the Web App, type the follwing code in your terminal:

    1. "python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db" # to clean & store data
    2. "python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl"  # to train the data
    3. "python app/run.py" # to run the Web App
    4. Finaly go to go to http://0.0.0.0:3001/ , where the App is hosted


## Licensing <a name="Licensing"></a>
All credits for the datasets go to Figure Eight: https://www.figure-eight.com/
For licencing details please contact Figure Eight
