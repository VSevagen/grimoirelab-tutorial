---
layout: default
title: Change Requests Accepted
nav_order: 1
parent: Evaluate code development efficiency
grand_parent: Understanding Community Health
---

# Change Request Accepted
Question: How many accepted change requests are present in a code change?

Change requests are defined as in Change Requests. Accepted change requests are those that end with the corresponding changes finally merged into the code base of the project. Accepted change requests can be linked to one or more changes to the source code, those corresponding to the changes proposed and finally merged.

For example, in GitHub when a pull request is accepted, all the commits included in it are merged (maybe squashed, maybe rebased) in the corresponding git repository. The same can be said of GitLab merge requests. In the case of Gerrit, a change request usually corresponds to a single commit.

### Objectives
Volume of coding activity.
Accepted change requests are a proxy for the activity in a project. By counting accepted change requests in the set of repositories corresponding to a project, you can have an idea of the overall coding activity in that project that leads to actual changes. Of course, this metric is not the only one that should be used to track volume of coding activity.

### Implementation

#### Aggregators:
- Count. Total number of accepted change requests during the period.
- Ratio. Ratio of accepted change requests over total number of change requests during
  that period.

#### Parameters:
- Period of time. Start and finish date of the period during which accepted change
  requests are considered. Default: forever.
- Criteria for source code. Algorithm. Default: all files are source code. If we focus on
  source code, we need a criterion for deciding whether a file belongs to the source code
  or not.

#### Filters
- By actor type (submitter, reviewer, merger). Requires merging identities corresponding
  to the same actor.
- By groups of actors (employer, gender... for each of the actors). Requires actor
  grouping, and likely, actor merging.

#### Visualizations
- Count per time period over time
- Ratio per time period over time

These could be grouped by actor type or actor group by applying the filters defined above.
These could be represented as bar charts, with time running in the X axis. Each bar would
represent accepted change requests to change the code during a certain period (eg, a
month).