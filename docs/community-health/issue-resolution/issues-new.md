---
layout: default
title: Issues New
nav_order: 1
parent: Issue resolution
grand_parent: Understanding Community Health
---

# Issues New
Question: How many new issues are created during a certain period?

Projects discuss how they are fixing bugs, or adding new features, in tickets in the issue
tracking system. Each of these tickets (issues) are opened (submitted) by a certain
person, and are later commented and annotated by many others.

Depending on the issue system considered, an issue can go through several states (for
example, "triaged", "working", "fixed", "won't fix"), or being tagged with one or more
tags, or be assigned to one or more persons. But in any issue tracking system, an issue is
usually a collection of comments and state changes, maybe with other annotations. Issues
can also be, in some systems, associated to milestones, branches, epics or stories. In
some cases, some of these are also issues themselves.

At least two "high level" states can usually be identified: open and closed. "Open"
usually means that the issues is not yet resolved, and "closed" that the issue was already
resolved, and no further work will be done with it. However, what can be used to identify
an issue as "open" or "closed" is to some extent dependent on the issue tracking system,
and on how a given project uses it. In real projects, filtering the issues that are
directly related to source code is difficult, since the issue tracking system may be used
for many kinds of information, from fixing bugs and discussing implementation of new
features, to organizing a project event or to ask questions about how to use the results
of the project.

In most issue trackers, issues can be reopened after being closed. Reopening an issue can
be considered as opening a new issue (see parameters, below).

For example, "issues" correspond to "issues" in the case of GitHub, GitLab or Jira, to
"bug reports" in the case of Bugzilla, and to "issues" or "tickets" in other systems.

### Objectives
Volume of issues discussed in a project. Issues are a proxy for the activity in a project.
By counting issues discussing code in the set of repositories corresponding to a project,
you can have an idea of the overall activity in discussing issues in that project. Of
course, this metric is not the only one that should be used to track volume of coding
activity.

### Implementation

#### Aggregators:

- Count. Total number of new issues during the period.
- Ratio. Ratio of new issues over total number of issues during that period.

#### Parameters:

- Period of time. Start and finish date of the period during which issues are considered. Default: forever.

- Criterion for source code. Algorithm. Default: all issues are related to source code.
    If we focus on source code, we need a criterion for deciding whether an issue is related to the source code or not.

- Reopen as new. Boolean. Default: False.
    Criterion for defining whether reopened issues are considered as new issues.

#### Filters

- By actors (submitter, commenter, closer). Requires merging identities corresponding to
  the same author.
- By groups of actors (employer, gender... for each of the actors). Requires actor
  grouping, and likely, actor merging.

#### Visualizations

- Count per time period over time
- Ratio per time period over time

These could be grouped by applying the filters defined above. These could be represented
as bar charts, with time running in the X axis. Each bar would represent proposals to
change the code during a certain period (eg, a month).