# Automation & QA Developer Assessment Submission

## Overview

This repository contains my submission for the Automation & QA Developer Take-Home Assessment.

**GitHub Repository:**
https://github.com/niteshdk11/Oytra-submissions

**Loom Video Walkthrough:**
https://drive.google.com/file/d/1bciRQa3evVQ3N3eGP0PdmmPpYUgHEB-f/view?usp=sharing

## Task 1 – QA Debug Report

I performed manual exploratory testing on the RealWorld Conduit Demo Application. The testing covered user registration, authentication, article creation, article editing, article deletion, profile management, and input validation.

A total of five issues were identified and documented with:

* Steps to reproduce
* Expected vs actual behavior
* Severity assessment
* Suspected cause
* Supporting screenshots

A root cause analysis was also provided for one selected issue.

## Task 2 – n8n API Integration Workflow

An automated workflow was built in n8n using the GitHub REST API.

Workflow functionality:

1. Retrieves JavaScript repositories from GitHub.
2. Filters and keeps the top repositories using a JavaScript Code node.
3. Enriches repository data using a second API request.
4. Uses an IF node with a threshold of **250,000 stars** to classify repositories as Popular or Normal.
5. Sends a formatted digest to Telegram.
6. Implements retry and error-handling mechanisms to improve workflow reliability.

## Bonus Task – Uptime Monitor

A second n8n workflow was created to monitor the availability of the RealWorld Conduit Demo Application.

Workflow functionality:

1. Executes automatically every 5 minutes.
2. Sends an HTTP request to the monitored application.
3. Checks the response status.
4. Sends a Telegram alert if the application becomes unavailable.
5. Includes retry logic to handle temporary failures.

## Repository Contents

* Task 1 QA Report
* Task 2 n8n Workflow Export
* Bonus Uptime Monitor Workflow Export
* Workflow Screenshots
* Execution Screenshots
* Supporting Documentation

Thank you for reviewing my submission.
