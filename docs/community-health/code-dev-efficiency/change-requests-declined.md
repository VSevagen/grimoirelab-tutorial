---
layout: default
title: Change Requests Declined
nav_order: 2
parent: Evaluate code development efficiency
grand_parent: Understanding Community Health
---

# Change Requests Declined
Question: What change requestsended up being declined during a certain period?

Change requests are defined as in Change Requests. Declined change requests are those that are finally closed without being merged into the code base of the project.

For example, in GitHub when a pull request is closed without merging, and the commits referenced in it cannot be found in the git repository, it can be considered to be declined (but see detailed discussion below). The same can be said of GitLab merge requests. In the case of Gerrit, code reviews can be formally "abandoned", which is the way of detecting declined change requests in this system.

### Objectives
Volume of coding activity. Declined change requests are a proxy for the activity in a project. By counting declined change requests in the set of repositories corresponding to a project, you can have an idea of the overall coding activity in that project that did not lead to actual changes. Of course, this metric is not the only one that should be used to track volume of coding activity.

### Implementation