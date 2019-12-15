# IT-Trends

### Table of Contents

1. [Installation](#installation)
2. [Motivation](#motivation)
3. [Files](#files)
4. [Results](#results)
5. [Licensing](#licensing)

## Installation <a name="installation"></a>
The .py scripts should be run in linux terminal

## Motivation <a name="Motivation"></a>
This Project is a classification engine that processes social messages in times of disaster. 
The algorithm classifies messages into more than 30 different categories based on their content.
Each category represents a type of help/support which needs to be provided in times of disaster.
The goal is to be able to quickly respond to a large amount of messages and provide adequate help.

## Files
1- Attached are two .csv files which contain the messages which are labeled into 36 different categries. 

2- There is also the "Code and Files.zip" file which contains the following files and folders:

    folder "data"   - contains the "process_data.py" script which cleans the data
    folder "models" - holds the "train_classifier.py" script which transform the text data and applies a classification model.
    folder "app"    - holds the "run.py" script which prepares data for the visualisation and the app, 
                      and also the go.html and master.html files whichprovide the visualisation and the app
    file "classifier.pkl"  - 
    file "Disaster response.db"

## Results


## Licensing <a name="Licensing"></a>

All credits for the datasets go to StackOverflow. 
The data is generally free to use, all licencing details can be found here:
https://www.kaggle.com/stackoverflow/stack-overflow-2018-developer-survey 
