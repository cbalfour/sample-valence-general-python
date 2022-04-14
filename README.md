# Sample Valence General Python

## Introduction

This project contains sample ID Key Authorization applications for the D2L BrightSpace LMS environment.

## Dependencies

Install the following dependencies via pip:

* d2lvalence
* d2lvalence_util
* beaker
* bottle
* requests


## Development Environment

BrightSpace has a developer instance at devcop.brightspace.com. To get full access - with various different account types do the following:
#. Join the BrightSpace Community [https://community.brightspace.com/]
#. Join the Developer group [https://community.brightspace.com/s/group/0F9610000001mZ1CAI]
#. Download the Developer Instance Credentials PDF file under Files in the Developer group site.

For more information see https://community.brightspace.com/s/article/New-Dev-Environment-for-Extensibility-Experimentation

### Register a ID Key Authorization application

#. Log into devcop.brightspace.com as user DevCoPAdmin
#. Click on the Admin Tools cog > Manage Extensibility
#. Click ID Key Authorization Tab
#. Register an app
* Application name: Random App Name
* Trusted URL: HTTP://localhost:8080/token
* Major version: 1
* Minor Version: 0 
* Description: Write something here if you wish
* Enable this application
* I accept the Non-Commercial Developer Agreement
* Click Register Application
#. An Application ID and Application Key are generated. Note these for use on the sample application configuration. 

### Update the sample application
Update the sample applications config_basic.py as follows:

* app_id: With the Application ID generated above
* app_key: With the Application Key generated above
* host: 'localhost'
* port '8080'
* lms_host: 'devcop.brightspace.com'
* lms_port: 443

#. Start up the application by pointing your browser at http://localhost:8080/
#. Click on the login link on the page
#. If you are not already logged into devcop.brightspace.com you will be asked to enter username and password. Use credentials for DevCoPStudent
#. If authentication is successful you should be redirected back to to the sample app 


