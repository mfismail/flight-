# Airline Flight Fare Prediction: 

![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-blue.svg) ![Python 3.6](https://img.shields.io/badge/Python-3.6-brightgreen.svg) ![Scikit-Learn](https://img.shields.io/badge/Library-ScikitLearn-orange.svg)

This repository consists of files required for end to end implementation and deployment of Machine Learning Flight Fare Prediction web application created with Flask and deployed on the Heroku platform.

## Table of Contents
  * [App Link](#app-link)
  * [About the App](#about-the-app)
  * [Deployement on Heroku](#deployement-on-heroku)
  * [Technologies Used](#technologies-used)

## App Link
If you want to view the deployed model, click on the following link:<br />
[https://flightfarepredictionismail.herokuapp.com/](https://flightfarepredictionismail.herokuapp.com/)

A glimpse of the web app:

![GIF](https://user-images.githubusercontent.com/58284020/132239862-4f086e2d-f083-4c42-b4d9-7a4429a2743f.png)

• If you encounter this webapp as shown in the picture given below, it is occuring just because **free dynos for this particular month provided by the Heroku platform have been completely used.** You can access the webpage on 1st of the next month.

• Sorry for the inconvenience.

![Heroku-Error](readme_resources/application-error-heroku.png)

## About the App
The Airline Flight Fare Prediction is a Flask web application to predict airline flight fares across the Indian cities. The dataset for the project is taken from Kaggle, and it is a time-stamped dataset so, while building the model, extensive pre-processing was done on the dataset especially on the date-time columns to finally come up with a ML model which could effectively predict airline fares across various Indian Cities. 
The dataset had many features which had to pre-processed and transformed into new parameters for a cleaner and simple web application layout to predict the fares. The various independent features in the dataset were: 

Airline: The name of the airline.

*Date_of_Journey: The date of the journey
*Source: The source from which the service begins.

*Destination: The destination where the service ends.
*Route: The route taken by the flight to reach the destination.
*Dep_Time: The time when the journey starts from the source.
*Arrival_Time: Time of arrival at the destination.
*Duration: Total duration of the flight.
*Total_Stops: Total stops between the source and destination.
*Additional_Info: Additional information about the flight
*Price: The price of the ticket

# Cleaning the Data
I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:

* Made Columns for Day and Month out of Date of Journey
* Calculated the total flight duration
* Removed the null values
* Removed the outliers

# Model Building
This project was challenging for me because all independent features were of categorical type. To convert it into numerical values LabelEncoder and OneHotEncoding were required. Also, it is not compulsory that we have to do import sklearn all the time and do the conversion.
Here I used RandomForest Regressor as my model and evaluated using Mean squared error.
And I done hyperparameter using Randomized SerachCV

The code is written in Python 3.6.10. 
If you don't have Python installed, you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:
```bash
pip install -r requirements.txt
```

## Deployement on Heroku
Login or signup in order to create virtual app. You can either connect your github profile or download ctl to manually to deploy this project.

[![](https://i.imgur.com/dKmlpqX.png)](https://heroku.com)

The next step would be to follow the instruction given in the [Heroku Documentation](https://devcenter.heroku.com/articles/getting-started-with-python) to deploy a web app.

## Technologies Used

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/flask-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) [<img target="_blank" src="https://number1.co.za/wp-content/uploads/2017/10/gunicorn_logo-300x85.png" width=280>](https://gunicorn.org) [<img target="_blank" src="https://scikit-learn.org/stable/_static/scikit-learn-logo-small.png" width=200>](https://scikit-learn.org/stable/) 
