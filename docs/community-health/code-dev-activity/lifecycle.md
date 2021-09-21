---
layout: default
title: Branch Lifecycle
nav_order: 1
parent: Evaluate code development activities
grand_parent: Understanding Community Health
---

# Branch Lifecycle
Question: How do projects manage the lifecycle of their version control branches?

This metric makes the lifecycle of version control branches visible. A branch lifecycle
includes acts of branch creation and deletion, as well as persistence of version control
branches. When writing code, a development team may create multiple branches, focused
around specific features. Subsequently, those branches may be merged into more persistent
branches, such as the main branch of a repository. Some branches persist for the life of
the repository, while others are deleted after code is merged into a more persistent
branch. By understanding these patterns, we can learn how branch creation, destruction,
and merging reflect the development practices of a particular project. A repository’s
typical branch lifecycle and management approach can be used to help identify a project’s
repository management style.

### Objectives
This metric’s objective is to increase the visibility of a repository’s volume and
frequency of branch creation and deletion, as well as persistence of version control
branches, in the context of other project characteristics. In turn, this helps potential
contributors understand how to initiate and sustain participation in a project. This
metric may help potential contributors understand how to initiate and sustain
participation in a project. Questions that can be addressed through this metric include:

- How many branches have been merged but not deleted?
- How long has a branch been merged and not deleted?
- How many branches have existed longer than a certain number of days, months, or years?
- How often do projects or repositories create branches?
- In the aggregate, how long do branches usually live?
- How can we distinguish between branch “death” (i.e., never intended to be used again;
  deletion) or branch “dormancy” (i.e., inactive for long periods of time, but may be used
  again) in cases where branches are infrequently deleted in a repository?

### Implementation

The stated advice regarding management of the branch lifecycle for a project may be
visible in a CONTRIBUTING.md document, and these documents can be compared across
repositories using linguistic analysis, and contrasted with data derived from actual
project practices to draw insights within, and across repositories. In most cases,
however, the data we focus on in this metric is quantitative in nature.

#### Aggregators:

- Count of branches created.
- Count of branches deleted.
- Count of branches merged.
- Count of branches abandoned (had unique commits, but never got merged before it was
  deleted)
- Total count of branches.
- Average age of open branches.
- Ratio at which branches are created vs. deleted.

#### Parameters:

- Period of time. Start and finish date of the period. Default: forever.
- Period during which change requests are considered.