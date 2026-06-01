# Task 2 – n8n API Integration Workflow

## Overview

This workflow was built in n8n to demonstrate API integration, data transformation, conditional routing, notification delivery, and error handling.

## APIs Used

1. GitHub Search Repositories API – Used to fetch the most starred JavaScript repositories.
2. GitHub Repository Details API – Used to enrich repository information with additional details.

## Workflow Logic

1. A Schedule Trigger runs the workflow automatically.
2. The first HTTP Request retrieves GitHub repository data.
3. A JavaScript Code node filters and keeps the top 5 repositories.
4. A second HTTP Request enriches the repository data.
5. An IF node classifies repositories based on a star-count threshold.
6. Results are grouped into:

   * Popular GitHub Repositories
   * Normal GitHub Repositories
7. The final digest is sent to Telegram using a Telegram Bot.

## Transformation

The workflow filters the GitHub API response and keeps only the top 5 repositories based on popularity. The results are then categorized according to a predefined star threshold.

## Error Handling

Error handling was implemented using n8n node settings and retry mechanisms to prevent silent workflow failures. Failed API requests can be retried and logged, ensuring reliable workflow execution.

## Output

The workflow sends a structured GitHub repository digest to Telegram, making it easy to monitor repository popularity and trends.
