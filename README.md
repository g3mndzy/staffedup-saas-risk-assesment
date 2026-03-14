# staffedup-saas-risk-assesment
Cybersecurity Intern Project with Riipen


Conducting a vulnerability assessment can be very daunting. Through our strategic questioning, we were able to get valuable data on their attack surface. Next is to use commonly used frameworks to identify any potential risks. 

# Platform Architecture 
Code hosting: Linode
Assets / data: AWS

## Application Stack
Backend: Nest JS
Frontend: React
Mobile: Flutter
Database: MySQL

## Environments: 
Dev, Staging, Production

#Authentication and Access

# Login Methods
Users authenticate with user/password
OAuth

Notes: No multi-factor authentification

## User roles
Master Admin
Enterprise Admin
Enterprise Sub user
Single Account Admin
Applicant

# Data Handling
They store: 
Name
Email
Address
Birthday
Employment information
References
SSN in onboarding documents

## Data Storage
AWS cloud storage

## Payment Data
handled by stripe so in compliance with PCI-DSS

# APIs and Integration
JWT tokens
rate limit: 100 requests per minute per IP
User tokens expire after 24 hours

# Microservices Architecture
They migrated to microservices, NestJS backend


Okay so lets break this down because what does this actually mean. Below describes the flow of traffic. 

users interact with the screen which send requests to the backend and the backend talks to database and storage. backend send data back to the screen .

React frontend = the web app users see in their browser
Flutter mobile application = the mobile app users use on phones
NestJS backend microservices = the server-side logic that processes requests
MySQL database = where structured data is stored
Linode = where some of the application code/infrastructure runs
AWS cloud services = where assets and applicant data are stored
