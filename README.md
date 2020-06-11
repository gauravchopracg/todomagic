# TodoMagic

This repository contains files on a “Todo” web application which has a user registration and login
functionalities, to add/delete/rank(prioritize) tasks in the todo list and also to share a todo list
over email from the web-app itself.

Live web app is here:
[Website](http://todomagic.herokuapp.com/)


# Building the web application

Web application has been developed with Python and Flask framework. The project has been developed using the tutorial [Flask Mega-Tutorial for Python 3.6](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)

**To run the app in you computer:**

1. Clone the repo

```bash
git clone https://github.com/gauravchopracg/todomagic.git
cd todomagic/
```

2. Create and activate virtual environment
```bash
virtualenv venv
venv\Scripts\activate
```

3. Install Dependencies
```bash
pip install -r requirements.txt
```

4. Config variables in .flaskenv file to support email functionalities
FLASK_APP=todomagic.py
MAIL_SERVER=smtp.googlemail.com
MAIL_PORT=587
MAIL_USE_TLS=1
MAIL_USERNAME=########@gmail.com
MAIL_PASSWORD=#####

5. Create migration repository
```bash
flask db init
flask db migrate
flask db upgrade
```

6. Run and play with it
```bash
flask run
```


## Deployment on heroku

To deploy the application on the Heroku

1. Creating Heroku account

Go to heroku.com and create a free account.

2. Installing the Heroku CLI

Heroku provides a command-line tool for interacting with their service called Heroku CLI, ava


The web application is deployed to Heroku cloud platform. A developer API using flask has been implemented, which returns a JSON containing a python dictionary in which key is URL of post and values are predicted flair. 

Can be accessed by querying POST request: 
```
import requests

files = {'upload_file': open('test.txt','rb')}
r = requests.post("http://rdflair.herokuapp.com/automated_testing", files=files)
```


