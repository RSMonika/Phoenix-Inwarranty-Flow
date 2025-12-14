# Postman API Automation Integration with GitHub Actions #
This repository is a Demonstartion for POC for integrating postman tests with github actions.
The tests are written in postman and they are exceuted on the virtual machine with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push to the main branch.You can also execute project manually using workflow dispatch.
The projects run on scheduled time with the help of cron jobs.
The HTML Report is archived and kept in the artifact section for the team to download it.
Along with that they can view the report directly from the github page "https://rsmonika.github.io/Phoenix-Inwarranty-Flow/".
The latest report is mailed to the team members using gmail SMTP.

## About Me ##
Hi I am Monika. I have 3 years of experience in Automation Testing and DevOps.
My Skillset includes UI Automation with Selenium Webdriver and for API Testing Used Rest assured and Postman.
You can connect with me over:(https://www.linkedin.com/feed/)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data driven testing with CSV
5. Schema Validation
6. Secret Management with GitHub Secrets


## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV for data driven testing
9. AWS EC2 instance for Self hosted github runner

## GitHub Pages ##
You can directly view the latest report of the Postman Test at the GitHub Page link:"https://rsmonika.github.io/Phoenix-Inwarranty-Flow/".

## HTML Report ##
The Report will be created in the newman folder

![Postman_Report](https://github.com/RSMonika/Phoenix-Inwarranty-Flow/blob/Static-Content/newman_report.png).

![Postman_Report](https://raw-githubusercontent.com/RSMonika/Phoenix-Inwarranty-Flow/Static-Content/newman_report.png)

## Project Structure ##
```
Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection Test Copy.postman_collection.json ## Collection File 
├─ QA.postman_environment.json  ## Environment File
└─ testdata.csv  ## Test data File

```


## How to run the project ##
You can run the project on your local system for that:
1. Clone the project on local system:"https://github.com/RSMonika/Phoenix-Inwarranty-Flow.git"
2. Install Nodejs and NPM "https://nodejs.org/en"
3. Install Newman using ```npm install -g newman```
4. Install Newman-Reporter-Htmlextra using ```npm install -g newman-reporter-htmlextra```
5. Run the Newman Command
   ```
              newman run 'Inwarranty-flow Collection Test Copy.postman_collection.json' \
              -e QA.postman_environment.json \
              -d testdata.csv \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html
   ```











