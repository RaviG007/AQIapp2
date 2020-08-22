Air-Quality-Index-Prediction
Webapp to predict the Air Quality Index of a region given climate conditions.

Environment setup:

requirements.txt: needed only for deployment to Heroku (not needed for local) as there were issues with anaconda installation on it.
requirements-conda.txt: needed for local development as I used conda locally. Run: conda create --name <env_name> --file requirements-conda.txt

For this project, I have followed the whole lifecycle of a Data Science Project.

1.Data Collection: (execute main-aqi.py)
For this step, I have written a web scrapper that scraps en.tutiempo.net for climate data from 2013 to 2015 and creates a HTML file for each month.

2.Data Preprocessing: (execute main-aqi.py)
Collected data which contained hourly measurements of AQI.
This was converted into a dictionary format where the dictionary key is the year and values are the daily AQI values.
Next, the data in step 1 was combined with data of this step to create a new CSV file.

3.Data Cleaning: (execute main-aqi.py)
The CSV file created in step 2 was cleaned to remove null values and improper data. A new resultant CSV file was created.

4.Feature Engineering and Model Creation: (execute individual jupyter notebooks)
Used algorithms Random Forest Regressor which gave best performance.

5.Model Deployment: 
Used HTML and css frontend to make API calls to Flask REST API backend.
Finally deployed on Heroku platform.
You can enter various climate details for prdiction od AQI for Bangalore city. Finally, click submit button and get your results for Air Quality Index.

Demo: link 1(for real time AQI)- https://aqiappcss.herokuapp.com/
			link 2(Predicted AQI from 2013 to 2016- https://aqipredictiondeploy.herokuapp.com/
