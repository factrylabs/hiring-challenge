# Data collector administration
For this coding test, we need you to design a single page application to list and create Factry Historian data collectors.

Some context, but not strictly relevant for this challenge: a collector is a service running on the Factry customer's infrastructure that collects data from their industrial equipment. The type of collector impacts the required settings for that collector.

## What is requested
Send us a link to a git repository that we can access so we can track your development. Provide documentation on how we can run your application. Take as long as you need to show your development skills.

## How it should work

First, we need to be able to log in. Once logged in, we want your application to show an overview of the collectors that are currently created. Lastly, your application should allow us to create a new collector.

## APIs
For this assignment, you will need to interface with 3 endpoints. They are available at  https://demo.factry.io/hiringchallenge/

1. A HTTP POST request to the `auth/login` endpoint to login.

The form body should consist of a username and password, which you should have received when briefed of this assignment. Upon successful auth on the backend, you will receive a [JWT token](https://jwt.io/) on the response body.

2. A HTTP GET request to the `historian/collectors` endpoint

Perform a GET request to retrieve all collectors from the historian administation system. Provide the JWT token as a http header to authenticate the request.

3. A HTTP POST request to the `historian/collectors` endpoint

Create a new collector by providing the appropriate JSON body in the request. Provide the JWT token as a http header to authenticate the request. Examples can be found in the `request-response` folder.

Examples of requests and responses can be found in the `request-response` folder.

## Questions?

Please contact us if anything is not clear.
