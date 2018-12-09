# PomaFocus #

## Introduction:

* The goal of PomaFocus is to help user to be more productive. To achieve this, the PomaFocus helps user to adapt Pomodoro technique easily by scheduling and rescheduling the tasks for user, providing proper reminders and monitoring the status of tasks.
* PomaFocus will manage scheduling of tasks, notifications, and approximate timing to completion. The tool will be integrated with Google calendar, which will allow it to schedule tasks around existing meetings.
* Each task won’t necessarily be complete within 25 minutes, thus, the tool will make sure to keep track of how many pomodoros (25 minute intervals) it took to complete the task.
[PomaFocus](http://pomafocus.com/) is a highly intelligble fully functioning task management service. It builds upon the ideas of [pomodoro technique](https://francescocirillo.com/pages/pomodoro-technique). Through PomaFocus, not only you create projects/ tasks, but we schedule your day/ week out for you! That way you can be more productive and focus on the tasks at hand.

 ## Table of content
- [Project Logistics](#project-logistics)
- [Features](#features)
- [Prerequisites for Set Up](#prerequisites-for-set-up)
- [Backend Set Up](#backend-set-up)
- [Frontend Set Up](#frontend-set-up)
- [Screenshots](#screenshots)
 ## Project Logistics

 ###### University Name
[http://www.sjsu.edu/](http://www.sjsu.edu/)

 ###### Course
[Cloud Technologies](http://info.sjsu.edu/web-dbgen/catalog/courses/CMPE281.html)

 ###### Professor
[Sanjay Garje](https://www.linkedin.com/in/sanjaygarje/)

 ######  ISA
[Anushri Srinath Aithal](https://www.linkedin.com/in/anushri-aithal/)

 ###### Students
- [Navjot Bola](https://www.linkedin.com/in/navjotbola/)
- [Parvizsho Aminov](https://www.linkedin.com/in/parvizsho/)
- [Dipti Shiralkar](https://www.linkedin.com/in/diptivs/)
- [Meghana Ynarasimha](https://www.linkedin.com/in/ymeghana/)

 ## Features
- Project Creation
- Task Creation
- Task Management
- Task Scheduling
- Amazon Lex for configuration
- Calendar view
- Task notifications/ reminders
- Integrated task start/ stop timers

## Architecture:

![architecture](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/architecture.png)

## Prerequisites for Set Up:
[Install NPM](https://www.npmjs.com/get-npm)

[Download/ Install node](https://nodejs.org/en/download/)


1. **Configure your machine using AWS admin account:**
  ```bash
  aws configure
  ```
2. **Create an S3 bucket to upload the app**
3. **Configure CloudFront to serve out app by using Static S3 website as origin**
4. **Point the domain with Route 53 to CloudFront**
5. **Create certificate using certificate manager and point to that on cloudfront to serve app over HTTPS**

## Backend Set Up:
1. **checkout the source code:**
  ```bash
  git clone https://github.com/diptivs/cucumber
  ```
2. **cd into the directory:**
  ```bash
  cd cucumber
  ```
3. **intall dependencies:**
  ```bash
  npm install
  ```
  ```bash
  npm install -g serverless
  ```
4. **test APIs locally:**
  ```bash
  serverless invoke local --function createUser --path mocks/users/createUser-event.json
  ```
5. **deploy:**
  ```bash
  serverless deploy --stage $DEPLOYMENT_STAGE
  ```

## Frontend Set Up:
1. **checkout the source code:**
  ```bash
  git clone https://github.com/diptivs/carrot
  ```
2. **cd into the directory:**
  ```bash
  cd carrot
  ```
3. **intall dependencies:**
  ```bash
  npm install
  ```
4. **run the server:**
  ```bash
  npm run start
  ```
5. **navigate to http://localhost:3000/:**

## Screenshots:
 ###### Signup
![signup](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/signup.png)
 ###### Login
![login](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/login.png)
 ###### Calendar
![calendar](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/calendarview2.png)
 ###### Add Tasks
![addtask](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/addtask.png)
 ###### Add Projects
![addproject](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/addproject.png)
 ###### Timer
![timer](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/timer.png)
 ###### No tasks under project view
![empty](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/emptymanage.png)
 ###### Manage Project View
![mange](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/manageview.png)
 ###### Overall Tasks View
![tasks](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/taskview.png)
 ###### Prioritze Tasks View
![priority](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/priorityview.png)
 ###### Task View
![taskview](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/taskseditview.png)
 ###### Amazon Lex Bot Integration
![bot](https://raw.githubusercontent.com/diptivs/pomafocus/master/screenshots/configuration.png)
