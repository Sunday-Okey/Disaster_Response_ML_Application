# Disaster Response ML Pipeline Project - An example of AI For Good
## Real-life use of a machine learning model to combat natural disasters

## The Current Problem

In 2021, there was a total of 401 natural disasters events worldwide. The Asian Pacific region experienced the highest number of natural disasters, most likely due to its size and susceptibility. Natural disasters affect almost every part of the world. In 2021, Haiti saw the highest number of deaths from a single natural disaster due to the earthquake that occurred there in August. The most expensive natural disaster in the United States was Hurricane Katrina in 2005, which caused immense destruction over a large area. In the decade 2010-2019, North American Hurricanes accounted for four out the five most costly natural disasters.

During or following a natural disaster, millions of people communicate either directly or via social media to get some help from the government or disaster relief and recovery services. If the affected person is tweeting it or even sending a message to the helpline service chances are that the message will be lost in the thousands of messages received. Sometimes it’s because a lot of people are just tweeting and very few people are needing help and organizations do not have enough time to filter out these many messages manually.

## Introduction
This project is part of the Udacity's Data Scientist Nanodegree Program in collaboration with Appen Formally Figure Eight. A big thanks to them for this amazing project!

With all the discussions about the dangers and ethics around emerging artificial intelligence and Machine Learning technologies, we sometimes forget all the good that AI is doing in the world. In this project, my goal is to analyze thousands of real messages provided by [Appen](https://appen.com/) formally Figure 8 that were sent during natural disasters either via socia media or directly to the disaster response organization. Essentially, I will use pre-labeled disaster messages to build a disaster response model that can categorize messages received in real time during a natural disaster event, so that messages can be sent to the right disaster response agency.

First and foremost, I will first explore the data and learn how it's recorded. Next, I will apply a series of transformations and preprocessing techniques to manipulate the data into a workable format. I will then build data or ETL Pipeline that processes the message and category data from CSV files, and load them into a SQlite database. Afterwards, I will build a Machine Learning Pipeine using Supervised Learning techniques to read data from the database to create and save a multi-output Supervised Learning Model, and deploy the solution into a Flask Web App. Finally, the web app will extract the data from the database to provide visualizations and use my model to classify new unseen messages for the 36 categories.

Machine Learning is critical to helping different organizations understand which messages are relevant to them and which messages to prioritize. Indeed this is amazing project with real-world significance!

This project includes a web application where disaster response worker can input messages received and get classification results. I will outline some of the work we are doing at Esri using AI for improving disaster response.

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
