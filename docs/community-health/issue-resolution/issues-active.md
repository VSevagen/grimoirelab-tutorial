---
layout: default
title: Issues Active
nav_order: 2
parent: Issue resolution
grand_parent: Understanding Community Health
---

# Issues Active
Question: How many issues were active during a certain period?

Issues are defined as in Issues New. Issues showing some activity are those that had some
comment, or some change in state (including closing the issue), during a certain period.

For example, in GitHub Issues, a comment, a new tag, or the action of closing an issue, is
considered as a sign of activity.

### Objectives
Volume of active issues in a project. Active issues are a proxy for the activity in a
project. By counting active issues related to code in the set of repositories
corresponding to a project, you can have an idea of the overall activity in working with
issues in that project. Of course, this metric is not the only one that should be used to
track volume of coding activity.

### Implementation

#### Aggregators:
- Count. Total number of active issues during the period.
- Ratio. Ratio of active issues over total number of issues during that period.

#### Parameters:
- Period of time. Start and finish date of the period during which issues are considered.
  Default: forever.
- Criteria for source code. Algorithm. Default: all issues are related to source code. If
    we focus on source code, we need a criterion for deciding whether an issue is related
    to the source code or not.

#### Filters
- By actor (submitter, commenter, closer). Requires merging identities corresponding to
  the same author.
- By groups of actors (employer, gender... for each of the actors). Requires actor
  grouping, and likely, actor merging.

#### Visualizations
- Count per period over time
- Ratio per period over time

These could be grouped by applying the previously defined filters. These could be
represented as bar charts, with time running in the X axis. Each bar would represent
proposals to change the code during a certain period (eg, a month).