# Postman API Automation Integration with Github Action #

This repository is a demonstration for POC for integration tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-html. 
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The Projects runs on a scheduled time with the help of cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly fron the github page: https://idavinde.github.io/Phoenix-Inwarranty-Flow./ .
The latest report is emailed to the team members using GMAIL SMTP.

## About Me ##
Hi, my name is Davinder Raju. I  have 5+ years of experience in Manual and Automation Testing. My skillset includes UI Automation with Selenium Webdriver. For API Testing I use Rest Assured and Postman.
You can connect with me over : (https://www.linkedin.com/in/davinder-raju/)

## Testing Coverage ##
1. Happy Flow Testing
2. Neagtive Testing and Edgecase Testing
3. Token Testing
4. Data Driven Testing
5. Schema Validation
6. Secrets Management with github Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Html
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for Self hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link: https://idavinde.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##

The Report will be created in newman folder
![Postman Report](https://github.com/idavinde/Phoenix-Inwarranty-Flow./blob/static-content/Html_Report.png)

## Project Structure ##

```
Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection.json  # Collection File 
├─ QA.postman_environment.json  # Environment File
└─ testdata.csv
```

## How to run the Project? ##
You can run the project on your local system for that:
1. Clone the Project on Local System: https://github.com/idavinde/Phoenix-Inwarranty-Flow..git
2. Install Nodejs and NPM from https://nodejs.org/en.
3. Install Newman using ``` npm install -g newman ```
4. Install Newman-Reporter-html ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman commands:
    ```
              newman run 'Inwarranty-flow Collection.postman_collection.json' \  
              -e QA.postman_environment.json \
              -d testdata.csv \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html
   ```


