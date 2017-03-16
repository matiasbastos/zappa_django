# Just a Zappa + Flask test

This will deploy a simple Flask app in AWS Lambda + API Gateway.

## Setup
    # configure your AWS keys
    $ aws configure
	# make a virtualenv
	$ virtualenv env
	$ source env/bin/activate
	# install dependencies
	$ pip install -r requirements.txt	

## Deploy WSGI App
    # deploy API to dev environment
    $ zappa deploy dev

    # Zappa will creates the API Gateway url for you similar to this
    $ curl https://123456.execute-api.us-west-2.amazonaws.com/dev

## Monitor Log
    # check dev environment
    $ zappa tail dev

## Deploy WSGI App
    # update API code to dev environment
    $ zappa update dev
