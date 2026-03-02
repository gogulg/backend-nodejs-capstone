---
name: User Story
about: This template defines a user story
title: ''
labels: ''
assignees: ''

---

**As a** registered user  
**I need** to log into my account  
**So that** I can access my dashboard  

### Details and Assumptions
* Users must already be registered  
* Users must enter a valid email and password  

### Acceptance Criteria (Gherkin)

Given a registered user is on the login page  
When the user enters a valid email and password  
Then the user should be redirected to the dashboard  

Given a registered user enters an invalid password  
When the user submits the login form  
Then an error message should be displayed  

Given a user is not registered  
When the user attempts to log in  
Then access should be denied  
