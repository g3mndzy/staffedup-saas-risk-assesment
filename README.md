# staffedup-saas-risk-assesment
Cybersecurity Intern Project with Riipen


Conducting a vulnerability assessment can be very daunting. Through our strategic questioning, we were able to get valuable data on their attack surface. Next is to use commonly used frameworks to identify any potential risks. We are to use SOC 2 and PCI-DSS. 

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

Users interact with the screen which send requests to the backend and the backend talks to database and storage. backend send data back to the screen .


# Company stack flow
React frontend = the web app users see in their browser
Flutter mobile application = the mobile app users use on phones
NestJS backend microservices = the server-side logic that processes requests
MySQL database = where structured data is stored
Linode = where some of the application code/infrastructure runs
AWS cloud services = where assets and applicant data are stored



The front end is the user facing side of an application (aka the actual website being interacted with). React js is being used which uses jasccript.Flutter is an open souce google UI toolkit for building mobile applications.Nest js is used for the back end which is the code that runs on the server.
** design a draw.io picture that describes a scenario of flow of data. 


## Considerations for Front end
1. can users input harmful data into forms?
2. is sensitive information exposed in the browser?
3. are there XSS risks?
4. are there insecure calls being made to the backend?

## Considerations for Mobil Applications
1. are API calls secure?
2. are tokens stored safely on the phone?
3. is sensitive data cached on the device?
4. can someone reverse-engineer the app?

## Considerations for Back End
1. how services authenticate to each other
2. whether internal APIs are protected
3. whether secrets are stored safely
4. whether one compromised service could affect others

## Considerations for Database
1. SQL injection
2. over-privileged access
3. weak encryption
4. poor backups
5. data leakage
6. access logging

## Considerations for linode
1. patching
2. server hardening
3. firewall rules
4. open ports
5. secrets in environment variables
6. network exposure

## Considerations for AWS 
1. are storage buckets private?
2. is data encrypted at rest?
3. who can access uploaded files?
4. are permissions least privilege?
5. are SSN documents stored securely?

   
The React frontend and Flutter mobile app are the user-facing parts of the platform. They send requests to the NestJS backend, which handles the business logic, authentication, and communication with other systems. The backend interacts with the MySQL database for structured records and AWS cloud services for storing assets and applicant-related files. The application infrastructure is hosted across Linode and AWS, which means the security assessment should consider both application-level risks and cloud configuration risks




| Risk                                      | Likelihood | Impact | Risk Level |
| ----------------------------------------- | ---------- | ------ | ---------- |
| Account takeover due to lack of MFA       | High       | High   | Critical   |
| Exposure of sensitive applicant documents | Medium     | High   | High       |
| Token theft due to long JWT expiration    | Medium     | Medium | Medium     |
| API scraping or abuse                     | Medium     | Medium | Medium     |
| Cloud storage misconfiguration            | Low        | High   | Medium     |


| ID   | Vulnerability                                              | Risk Level | Impact                                          |
| ---- | ---------------------------------------------------------- | ---------- | ----------------------------------------------- |
| V-01 | No multi-factor authentication for administrative accounts | High       | Increased risk of account takeover              |
| V-02 | Storage of SSN documentation                               | High       | Potential exposure of sensitive personal data   |
| V-03 | JWT tokens valid for 24 hours                              | Medium     | Session hijacking risk if token is stolen       |
| V-04 | API rate limit only by IP                                  | Medium     | Distributed attacks may bypass limits           |
| V-05 | OAuth authentication reliance                              | Medium     | Misconfiguration could allow unauthorized login |
| V-06 | Hybrid cloud architecture                                  | Medium     | Misconfiguration risk between Linode and AWS    |

| Asset                 | Description                                    | Sensitivity |
| --------------------- | ---------------------------------------------- | ----------- |
| Applicant Portal      | Web interface for job seekers to apply         | High        |
| Employer Dashboard    | Recruiter and hiring manager interface         | High        |
| Authentication System | Handles login and OAuth                        | Critical    |
| Backend Microservices | NestJS services managing application logic     | High        |
| Database              | MySQL storing applicant data                   | Critical    |
| Cloud Storage         | AWS storage containing uploaded documents      | Critical    |
| Payment Processing    | Subscription payments handled by Stripe        | High        |
| APIs                  | Internal APIs serving frontend and mobile apps | High        |

| Asset              | MITRE Tactic         | Potential Technique       | Example Scenario                         |
| ------------------ | -------------------- | ------------------------- | ---------------------------------------- |
| Login System       | Initial Access       | Credential Stuffing       | Attackers attempt stolen credentials     |
| Applicant Portal   | Execution            | Malicious File Upload     | Resume uploads containing malware        |
| Employer Dashboard | Privilege Escalation | Abuse of Role Permissions | Sub-user gains admin access              |
| API Gateway        | Discovery            | Endpoint Enumeration      | Attacker maps API structure              |
| Database           | Exfiltration         | Data Dump                 | Unauthorized export of applicant records |
| Authentication     | Credential Access    | Token Theft               | Stolen JWT used for account takeover     |
| Cloud Storage      | Collection           | Data Harvesting           | Public storage bucket exposure           |




Sources
https://www.codecademy.com/article/what-is-back-end-architecture
https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0
https://docs.nestjs.com

https://www.w3schools.com/whatis/whatis_frontenddev.asp
https://legacy.reactjs.org
