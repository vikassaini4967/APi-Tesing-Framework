# API-Testing-Framework

This is an Rest-API testing framework which is made from

- RestAssured
- TestNG
- Extent Reports
- Java Faker
- Github Actions


## Features:

- Slack integration: Get slack messages on each action (Report Deployment, Docker Deployment) after each test/build.
- Lastest Exection Report: Support for lastest exection report using Github Pages
- Docker Image: Support for automatic docker image build and push to docker hub using GithubActions



### Note:

- Please run this through TestNG XML, running individual tests from IDE will break the framework
- Since it depends on the TestNG listeners to start execution




## How to run:




Open Terminal in API-Testing-Framework and run (for detailed execution):

```
mvn -e -X clean test
```

To run the same in docker container use this image [DockerHub](https://hub.docker.com/r/heyrmi/apitestingframework). 
Open the terminal and make a seperate directory for test reports

```
mkdir TestReports && cd TestReports
docker run -v ${PWD}:/home/apiframework/Reports heyrmi/apitestingframework
```

## Reports: 

Report will be automatically published here: [Latest-Execution-Report](https://heyrmi.github.io/API-Testing-Framework)

This is done through Github Actions.
