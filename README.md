# Skillx Lab infra

## Install the Heroku CLI
Download and install the Heroku CLI from https://devcenter.heroku.com/articles/heroku-command-line

## Create a python environment

`$python3 -m venv .venv`

Ensure you have the latest buildtools and install python modules below.

`pip install — upgrade setuptools pip`

`pip install cryptography`

`pip install psycopg2`

`pip install apache-superset`


## Clone this project to your local machine

`$ git clone https://github.com/muchemwal/skillx.git  .`

Ensure you set your own SECRET_KEY in the superset_config.py file, use the python code below to generate your own key

`$python`

  ````from cryptography import fernet````

  ````   fernet.Fernet.generate_key()````

## Create your app on Heroku and login via a terminal as below.

`$heroku login`

`$heroku create <your app name>`

`$heroku addons:create heroku-postgresql:hobby-dev`

`$ git add .`

`$ git commit -am "make it better`

`$ git push heroku master`

Add an Admin user from heroku terminal

`'heroku run bash'`

`export FLASK_APP=superset`
`superset fab create-admin`
`superset init`
`exit`


## Deploy your changes
Make some changes to the code you just cloned and deploy them to Heroku using Git.

`$ git add .`
`$ git commit -am "make it better"`
`$ git push heroku master`
