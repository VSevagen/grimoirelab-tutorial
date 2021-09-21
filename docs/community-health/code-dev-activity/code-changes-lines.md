---
layout: default
title: Code Changes Lines
nav_order: 3
parent: Evaluate code development activities
grand_parent: Understanding Community Health
---

# Code Changes Lines
Question: What is the sum of the number of lines touched (lines added plus lines removed) in all changes to the source code during a certain period?

When introducing changes to the source code, developers touch (edit, add, remove) lines of
the source code files. This metric considers the aggregated number of lines touched by
changes to the source code performed during a certain period. This means that if a certain
line in a certain file is touched in three different changes, it will count as three
lines. Since in most source code management systems it is difficult or impossible to tell
accurately if a lines was removed and then added, or just edited, we will consider editing
a line as removing it and later adding it back with a new content. Each of those (removing
and adding) will be considered as "touching". Therefore, if a certain line in a certain
file is edited three times, it will count as six different changes (three removals, and
three additions).

For this matter, we consider changes to the source code as defined in Code Changes. Lines
of code will be any line of a source code file, including comments and blank lines.

### Objectives
Volume of coding activity: Although code changes can be a proxy to the coding activity of
a project, not all changes are the same. Considering the aggregated number of lines
touched in all changes gives a complementary idea of how large the changes are, and in
general, how large is the volume of coding activity.

### Implementation

#### Aggregators:
- Count. Total number of lines changes (touched) during the period.


#### Parameters:
- Period of time: Start and finish date of the period. Default: forever.
    Period during which changes are considered.
- Criteria for source code; Algorithm Default: all files are source code. If we are
    focused on source code, we need a criterion for deciding whether a file is a part of
    the source code or not.
- Type of source code change:
    - Lines added
    - Lines removed
    - Whitespace

#### Filters
- By actors (author, committer). Requires actor merging (merging ids corresponding to the
  same author).

- By groups of actors (employer, gender...). Requires actor grouping, and likely, actor merging.

- By tags (used in the message of the commits). Requires a structure for the message of
  commits. This tag can be used in an open-source project to communicate to every
  contributors if the commit is, for example, a fix for a bug or an improvement of a
  feature.

#### Visualizations
- Count per month over time
- Count per group over time

These could be represented as bar charts, with time running in the X axis. Each bar would
represent a code changes during a certain period (eg, a month).