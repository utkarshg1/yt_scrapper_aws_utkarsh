# YouTube Scraper Deployment on AWS by Utkarsh Gaikwad

This is YouTube Scrapper headless Deployed on AWS by me - Utkarsh Gaikwad

I used following Approach here :
1. AWS Lambda Function : This will serve as an API to me , my Flask app will send request to this custom API Created by me.
2. Elastic Beanstalk : This will serve my Flask Application which will display User Interface to Website.
3. Code Pipeline : For Continuous Deployment of Code from GitHub to AWS. 

# AWS Elastic Beanstalk Link

## Website Link : [http://utkarshgaikwadytscraping-env.eba-gm3aqm5x.us-east-1.elasticbeanstalk.com/](http://utkarshgaikwadytscraping-env.eba-gm3aqm5x.us-east-1.elasticbeanstalk.com/)

# YouTube Demo for this project 

## YouTube Demo Link : [https://youtu.be/X-7ZvUQZiYQ](https://youtu.be/X-7ZvUQZiYQ)

# Website is scraped based on my Lambda Function wirh Selenium and Chrome driver

API URL : [https://8rkvysfczg.execute-api.us-east-1.amazonaws.com/yt_scrapper_utkarsh](https://8rkvysfczg.execute-api.us-east-1.amazonaws.com/yt_scrapper_utkarsh)

GitHub Repo for my API : [https://github.com/utkarshg1/yt_scrapper_lambda_utkarsh](https://github.com/utkarshg1/yt_scrapper_lambda_utkarsh)

Note that above url is a POST request URL only. Documentiaton for API inside the above github Repository link 

Logic Explaination Behind API Notebook : [Logic Explaination Jupyter Notebook for API](https://github.com/utkarshg1/PWSkills-Assignments/blob/main/Assignment%2021%20-%2022%20February%202023/Assignment21Utkarsh.ipynb)

# Using my Above API in python:

Please check my below python code for using my above custom API:

~~~python
import requests
data = {'url':'https://www.youtube.com/@PW-Foundation/videos'}
my_api_url = 'https://8rkvysfczg.execute-api.us-east-1.amazonaws.com/yt_scrapper_utkarsh'
response = requests.post(my_api_url,json=data)
response.json()
~~~

# WebApp UI Homepage

![Homepage of my Web App](./UI%20Screenshots/HomePage.jpg)

# Testing the data for : [https://www.youtube.com/@PW-Foundation/videos](https://www.youtube.com/@PW-Foundation/videos)

![Results Screenshot](./UI%20Screenshots/TestResults.jpg)

# Testing for Tseries youtube Channel : [https://www.youtube.com/@tseries/videos](https://www.youtube.com/@tseries/videos)

![Results TSeries](./UI%20Screenshots/TestResultTseries.jpg)

# This App is deployed using Elastic Beanstalk and Code Pipeline

## Elastic BeanStalk Screenshot

![Elastic Beanstalk](./UI%20Screenshots/EBstalk.jpg)

## Code Pipeline

![Code Pipeline](./UI%20Screenshots/CodePipeline.jpg)
