---
layout: default
title: Issues Age
nav_order: 4
parent: Issue resolution
grand_parent: Understanding Community Health
---

# Issue Age
Question: How long have open issues been left open?

This metric is an indication of how long issues have been left open in the considered time period. If an issue has been closed but re-opened again within that period if will be considered as having remained open since its initial opening date.

### Objectives
When the issue age is increasing, identify the oldest open issues in a project to gain insight as to why they have been open for an extended period of time. Additionally, to understand how well maintainers are resolving issues and how quickly issues are resolved.

### Implementation
For all open issues, get the date the issue was opened and calculate the number of days to current date.

#### Aggregators:

- Average. Average age of all open issues.
- Median. Median age of all open issues.

#### Parameters:

- Period of time. Start and finish date of the period during which open issues are considered. Default: forever (i.e., the entire observable period of the project's issue activity).

#### Filters
- Module or working group
- Tags/labels on issue

#### Visualizations

1. Summary data for open issues<br />

    ![Summary data for open issues](../assets/issue-age_open-issue-data.png)

2. Count of open issues per day<br />

    ![Count of open issues per day](../assets/issue-age_open-issue-count-timeseries.png)