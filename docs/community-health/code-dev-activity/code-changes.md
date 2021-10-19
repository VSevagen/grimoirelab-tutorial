---
layout: default
title: Code Changes
nav_order: 1
parent: Evaluate code development activities
grand_parent: Understanding Community Health
---

# Code Changes
Question: How many changes were made to the source code during a specified period?

These are changes to the source code during a certain period. For "change" we
consider what developers consider an atomic change to their code. In other
words, a change is some change to the source code which usually is accepted and
merged as a whole, and if needed, reverted as a whole too. For example, in the
case of git, each "change" corresponds to a "commit", or, to be more precise,
"code change" corresponds to the part of a commit which touches files considered
as source code.

### Objectives
Volume of coding activity. Code changes are a proxy for the activity in a
project. By counting the code changes in the set of repositories corresponding
to a project, you can have an idea of the overall coding activity in that
project. Of course, this metric is not the only one that should be used to track
volume of coding activity.

#### Visualizations

#### Steps

1. Click on `Visualize` option in the sidebar and click on the `+` icon to
   create a new visualization.

2. Pick the `Vertical Bar` chart and select `git` as the index.

3. You'll be presented with the following default visualization.

  ![commit count](../assets/commit-count.png)

4. For `Metrics` set the aggregation to `Unique Count` and field to `hash`. Set
   the custom label as `Commits` as the current unique shows the total number of
   commits.

   ![metrics code changes](../assets/metrics-code-changes.png)

5. For `Buckets` select the bucket type `X-axis`.

6. Set the aggregation to `Date Histogram`, field to `grimoire_creation_date`
   and interval to `Auto`. Set the custom label to `Time`.

   ![bucket code changes](../assets/bucket-code-changes.png)

7. In the end, your visualization would look something like the this.

![code changes](../assets/code-changes.png)

