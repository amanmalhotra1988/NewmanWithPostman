# NewmanWithPostman
This repository is for quickly setting up the Newman integration with Postman Collections

-Assuming you have basic understanding of Postman [https://www.postman.com/], Creating Collections, Creating Environments

## How to install Newman
Prerequisite: 
Node.js should already installed on your Operating System <br>
* Download it from here [(https://nodejs.org/en/)]
* Install Node.js
* Go to Command Prompt
* Run Below command

npm install - g newman

## How to check the version of Newman
newman -v
newman -version

## Installing Newman HTML Reporter plugin for generating Newman Test Execution Report
npm install -g newman-reporter-html

## Save Collection and Environment File from the Postman- Export it from Postman
Save the Collection and Environment Files (Json Files) in one Folder

## Command to Run the Postman Collection
newman run collectionName.json -e environmentName.json - r htmlextra --reporter-htmlextra-browserTitle "ProjectName API Execution" --reporter-htmlextra-title "Project Name Execution Status-QA" --reporter-htmlextra-titleSize 1 --reporter-htmlextra-skipSensitiveData

## Reference Guides
https://postman-quick-reference-guide.readthedocs.io/en/latest/assertions.html#how-to-compare-value-of-a-response-against-multiple-valid-values

## If we want to run the Collection which have multiple folders
newman run collectionName.postman_collection.json -e environmentName.postman_environment.json --folder one

newman run collectionName.postman_collection.json -e environmentName.postman_environment.json --folder two
