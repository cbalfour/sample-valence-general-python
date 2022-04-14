# Sample Valence General Python

## Introduction

This project contains python sample [legacy](https://docs.valence.desire2learn.com/basic/legacyauth.html) ID Key Authorization applications for the D2L [BrightSpace](https://brightspace.com) learning management system (LMS) environment.

## Dependencies

Setup a Python 3 [virtual environment](https://docs.python.org/3/library/venv.html) and install the following dependencies via pip:
* d2lvalence
* d2lvalence_util
* beaker
* bottle
* requests

## Development Environment

BrightSpace has a developer instance at [devcop.brightspace.com](https://devcop.brightspace.com). 

To get full access - with account types including administrator, instructor and student - do the following:

1. Join the [BrightSpace Community](https://community.brightspace.com/)
1. Join the [Developer group](https://community.brightspace.com/s/group/0F9610000001mZ1CAI)
1. Download the Developer Instance Credentials PDF file under Files in the Developer group site.

For more information see [this](https://community.brightspace.com/s/article/New-Dev-Environment-for-Extensibility-Experimentation) BrightSpace Community article.

### Register a ID Key Authorization application

1. Log into [devcop.brightspace.com](https://devcop.brightspace.com) as user DevCoPAdmin
1. Click on the Admin Tools cog > Manage Extensibility
1. Click ID Key Authorization Tab
1. Register an app
* Application name: Random App Name
* Trusted URL: HTTP://localhost:8080/token
* Major version: 1
* Minor Version: 0 
* Description: Write something here if you wish
* Enable this application
* I accept the Non-Commercial Developer Agreement
* Click Register Application
1. An Application ID and Application Key are generated. Note these for use on the sample application configuration. 

### Update the sample application
Update the sample applications config_basic.py as follows:

* app_id: With the Application ID generated above
* app_key: With the Application Key generated above
* host: 'localhost'
* port '8080'
* lms_host: 'devcop.brightspace.com'
* lms_port: 443

1. Start up the application by pointing your browser at http://localhost:8080/
1. Click on the login link on the page
1. If you are not already logged into devcop.brightspace.com you will be asked to enter username and password. Use credentials for DevCoPStudent
1. If authentication is successful you should be redirected back to to the sample app 

## Application-specific Notes

### Basic

### ProfileChange

### FinalGrades

* lms_student_role_id: 110. Check this value via the roles [API](https://devcop.brightspace.com/d2l/api/lp/1.0/roles/)
* lms_course_offering_type_id: 

## Documentation 

1. [API Reference](https://docs.valence.desire2learn.com/reference.html)
