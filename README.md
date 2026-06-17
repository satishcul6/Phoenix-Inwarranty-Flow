# Postman API Automation Integration with GitHub Actions #
## This restrates a Proof of Concept (POC) for integrating Postman API automation tests with GitHub Actions ##

The API tests are written in Postman and executed using Newman along with the newman-reporter-htmlextra. GitHub Actions automates the execution on every push to the main branch, via manual trigger using workflow_dispatch, and through scheduled runs using cron jobs.

CI/CD Execution and Reporting
Postman collections are executed using Newman
HTML execution reports are generated using newman-reporter-htmlextra
Test reports are archived as GitHub Artifacts for download
Reports are published using GitHub Pages for easy access
Email notifications are sent to team members using Gmail SMTP
GitHub Actions manages the complete automation workflow

### Deployment and Reports ###
All deployments: https://github.com/satishcul6/Phoenix-Inwarranty-Flow/deployments

Latest HTML report (GitHub Pages): https://satishcul6.github.io/Phoenix-Inwarranty-Flow/

### About Me ###
Myself Satish Mishra, and I have Total 8 years of experience in IT and 6 years of Expereince in UI & API Automation along with CI/CD

My skill set includes:

UI Automation using Selenium WebDriver Java

API Automation Using Rest Assured Java , Postman , Newman

CI/CD automation using GitHub Actions , Jenkins , Azure DevOps

Test reporting and email notifications

Secrets management using GitHub Secrets

Connect with me: satishmishra372@gmail.com

### Testing Coverage ###

Happy flow testing

Negative and edge case testing

Authentication and token testing

Data-driven testing using CSV

Schema validation

Secure secrets management

### Technology Stack Used For POC ###

Postman

Node.js (v22)

Newman

Newman Reporter HTML Extra

GitHub Actions

Gmail SMTP

GitHub Pages

CSV-based data-driven testing

AWS EC2 self-hosted GitHub runner

HTML Report

The HTML report is generated inside the newman folder after execution. The latest report is always available via GitHub Pages, while previous reports can be downloaded from GitHub Artifacts.


### How to Run the Project Locally ###

Clone the repository:

git clone

Install Node.js and npm from: https://nodejs.org/en

Install Newman:

npm install -g newman
Install Newman Reporter HTML Extra:

npm install -g newman-reporter-htmlextra
Run the Newman command:

newman run "Inwarranty-flow Collection.postman_collection.json" \
  -e QA.postman_environment.json \
  -d testdata.csv \
  -r cli,htmlextra \
  --reporter-htmlextra-export ./newman/index.html
