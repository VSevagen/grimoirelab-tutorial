---
layout: default
title: Issues Closed
nav_order: 3
parent: Issue resolution
grand_parent: Understanding Community Health
---

# Issues Closed
Question: How many issues were closed during a certain period?

Issues are defined as in Issues New. Issues closed are those that changed to state closed
during a certain period.

In some cases or some projects, there are other states or tags that could be considered as
"closed". For example, in some projects they use the state or the tag "fixed" for stating
that the issue is closed, even when it needs some action for formally closing it.

In most issue trackers, closed issues can be reopened after they are closed. Reopening an
issue can be considered as opening a new issue, or making void the previous close (see
parameters, below).

For example, in GitHub Issues or GitLab Issues, issues closed are issues that were closed
during a certain period.

### Objectives
Volume of issues that are dealt with in a project. Closed issues are a proxy for the
activity in a project. By counting closed issues related to code in the set of
repositories corresponding to a project, you can have an idea of the overall activity in
finishing work with issues in that project. Of course, this metric is not the only one
that should be used to track volume of coding activity.

### Implementation

#### Aggregators:

- Count. Total number of closed issues during the period.
- Ratio. Ratio of closed issues over total number of issues during that period.
- Reactions. Number of "thumb-ups" or other reactions on issues.

#### Parameters:

- Period of time. Start and finish date of the period during which issues are considered.
  Default: forever.

- Criteria for source code. Algorithm. Default: all issues are related to source code. If
    we focus on source code, we need a criterion for deciding whether an issue is related
    to the source code or not. All issues could be included in the metric by altering the
    default.

- Reopen as new. Boolean, defining whether reopened issues are considered as new issues.
  If false, it means the closing event previous to a reopen event should be considered as
  void. Note: if this parameter is false, the number of closed issues for any period could
  change in the future, if some of them are reopened.

- Criteria for closed. Algorithm. Default: having a closing event during the period of interest.

#### Filters

- By actors (submitter, commenter, closer). Requires merging identities corresponding to
  the same author.
- By groups of actors (employer, gender... for each of the actors). Requires actor
  grouping, and likely, actor merging.

#### Visualizations

- Count per time period over time
- Ratio per time period over time

These could be grouped by applying the filters defined aboce. These could be represented
as bar charts, with time running in the X axis.