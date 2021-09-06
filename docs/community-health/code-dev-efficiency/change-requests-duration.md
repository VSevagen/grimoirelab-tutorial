---
layout: default
title: Change Requests Duration
nav_order: 3
parent: Evaluate code development efficiency
grand_parent: Understanding Community Health
---

# Change Requests Duration
Question: What is the duration of time between the moment a change request starts and the moment it is accepted or closed?

Change requests are defined as in Change Requests. Accepted change requests are defined in Change Requests Accepted.

The change request duration is the duration of the period since the change request started, to the moment it ended (by being accepted and being merged in the code base). This only applies to accepted change requests.

For example, in GitLab a change request starts when a developer uploads a proposal for a change in code, opening a change request. It finishes when the change request is finally accepted and merged in the code base, closing the change request.

In case there are comments or other events after the code is merged, they are not considered for measuring the duration of the change request.

### Objectives
Duration of acceptance of change requests. Review duration for accepted change requests is one of the indicators showing how long does a project take before accepting a contribution of code. Of course, this metric is not the only one that should be used to track volume of coding activity.

### Implementation