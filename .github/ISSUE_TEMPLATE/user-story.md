---
name: User Story
about: This template defines a user story
title: "Search Books by Author"
labels: enhancement
assignees: ''
---

**As a** customer  
**I need** to search for books by author  
**So that** I can quickly find books written by a specific author  

### Details and Assumptions
* The system contains a list of books stored in the database.
* Each book has an author field.
* The search should be case-insensitive.
* Partial author names should return matching results.

### Acceptance Criteria

Scenario: Search books by full author name
  Given the database contains books written by "J.K. Rowling"
  When the user searches for "J.K. Rowling"
  Then the system returns all books written by "J.K. Rowling"

Scenario: Search books by partial author name
  Given the database contains books written by "J.K. Rowling"
  When the user searches for "Rowling"
  Then the system returns all books written by "J.K. Rowling"

Scenario: Search returns no results
  Given the database contains no books written by "Unknown Author"
  When the user searches for "Unknown Author"
  Then the system returns an empty list
  And displays a message "No books found"
