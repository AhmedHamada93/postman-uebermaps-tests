# Uebermaps REST APIs Test
REST APIs tests using POSTMAN for [Uebermaps v2](https://uebermaps.com/api/v2/) [maps](https://uebermaps.com/api/v2#resource_Maps) and [comments](https://uebermaps.com/api/v2#resource_Comments) APIs.


## Dependencies
- [NodeJS]([https://nodejs.org/en/](https://nodejs.org/en/))
- [newman]([https://www.npmjs.com/package/newman](https://www.npmjs.com/package/newman)) `npm install -g newman`
- [newman-html-reporter]([https://www.npmjs.com/package/newman-reporter-html](https://www.npmjs.com/package/newman-reporter-html)) `npm install -g newman-reporter-html`

## Tests
To view requests and tests in POSTMAN
- Import > File > Upload Files > Select `Uebermaps.postman_collection.json`

## Tests Structure
- Single collection with pre-request script to get authorization token using username and password to be used in the requests.
- 2 folders for MAPS and COMMENTS apis.
 
## Run
- To run tests using newman CLI use `newman run Uebermaps.postman_collection.json -r html -e Dev.postman_environment.json` at **Uebermaps.postman_collection.json** directory.

## Bug Report
[Find Bug Report Here](https://git.toptal.com/screening/ahmed-hamada/blob/master/2_API_Tests/bug-report.md)

## Report
At collections directory you will find the generated html report at `newman\newman-run-report-timestamp.html` 

Find HTML report [here](https://git.toptal.com/screening/ahmed-hamada/blob/master/2_API_Tests/newman/newman-run-report-2020-09-15-20-54-12-722-0.html)

Report Examples

![report-screenshot-1](https://git.toptal.com/screening/ahmed-hamada/raw/master/2_API_Tests/newman/screenshot-1.png)

![report-screenshot-2](https://git.toptal.com/screening/ahmed-hamada/raw/master/2_API_Tests/newman/screenshot-2.png)