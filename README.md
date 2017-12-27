[![Build Status](https://travis-ci.org/JanRuettinger/chatanalytics.svg?branch=master)](https://travis-ci.org/JanRuettinger/chatanalytics)

# Chatanalytics
www.chatanalytics.io

## What does it do?
For now you can send a whatsapp group chat to chat@chatanalytics.io (detailed instructions on the website) and after some time you will get back a link to the result of the analysis of your group chat. The result page consists of five different plots.

## Why I created this project?
I created this project right after I went to EuroSciPy 17 to learn more about about the SciPy ecosystem, travis and testing.


## How to run the code?
You can't just copy the code and run it because you need to adjust some configs first (instance folder/factory.py) and probably reset some env variables. After you are done:


````
1. flask run
2. celery worker -A project.main.tasks.celery --loglevel=info
3. celery beat -A project.main.tasks.celery --loglevel=info
````
