
# CI/CD Pipeline using Jenkins for a Flask application

## Overview

This project demonstrates the implementation of a CI/CD pipeline for a simple Flask application using Jenkins. The pipeline automates the process of building, testing, and deploying the application whenever changes are pushed to the repository.

A minimal Flask application was created for this purpose.

---

## Repository

https://github.com/chandanbg/HeroViredAssignment-CICD-flask-app
---

## Jenkins Pipeline

The pipeline is defined using a Jenkinsfile in the root directory and consists of the following stages:

* Build: Creates a virtual environment and installs dependencies using pip
* Test: Executes unit tests using pytest
* Deploy: Runs the Flask application if tests pass

---

## Trigger Configuration

The pipeline is configured using Poll SCM.

Jenkins checks the repository at regular intervals and automatically triggers a build when changes are detected in the main branch.

---

## Email Notifications

Email notifications are configured using SMTP settings.

Notifications are sent on:

* Successful builds
* Failed builds

---

## Testing

Unit tests are written using pytest.
The deployment stage is executed only if all tests pass successfully.

---

## Deployment

The application is deployed locally and can be accessed at:

http://192.168.29.12:8081/

---

## Screenshots

<img width="1414" height="667" alt="image" src="https://github.com/user-attachments/assets/bb9a3a58-2dad-42ae-82ba-5da4f27f15cf" />

<img width="1366" height="537" alt="image" src="https://github.com/user-attachments/assets/82bb07c3-db89-463d-9854-ddb77566371d" />

<img width="1913" height="797" alt="image" src="https://github.com/user-attachments/assets/6c95cd48-16e7-458a-b02f-58956ebaa641" />

<img width="1856" height="816" alt="image" src="https://github.com/user-attachments/assets/b74a18c2-7581-4334-8182-0d7d3ef94b32" />

<img width="1884" height="818" alt="image" src="https://github.com/user-attachments/assets/0e62b995-0af0-4de2-8179-d58dd2a0c200" />

<img width="1903" height="821" alt="image" src="https://github.com/user-attachments/assets/b63d37f0-78c6-4c47-ba8c-6798e475bb26" />

---

## Conclusion

This demonstrates a complete CI/CD workflow using Jenkins, including automated build, test, deployment, and notifications.
