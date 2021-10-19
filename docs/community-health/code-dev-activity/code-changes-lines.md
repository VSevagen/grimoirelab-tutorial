---
layout: default
title: Code Changes Lines
nav_order: 2
parent: Evaluate code development activities
grand_parent: Understanding Community Health
---

# Code Changes Lines
Question: What is the sum of the number of lines touched (lines added plus lines
removed) in all changes to the source code during a certain period?

When introducing changes to the source code, developers touch (edit, add,
remove) lines of the source code files. This metric considers the aggregated
number of lines touched by changes to the source code performed during a certain
period. This means that if a certain line in a certain file is touched in three
different changes, it will count as three lines. Since in most source code
management systems it is difficult or impossible to tell accurately if a lines
was removed and then added, or just edited, we will consider editing a line as
removing it and later adding it back with a new content. Each of those (removing
and adding) will be considered as "touching". Therefore, if a certain line in a
certain file is edited three times, it will count as six different changes
(three removals, and three additions).  

For this matter, we consider changes to the source code as defined in Code
Changes. Lines of code will be any line of a source code file, including
comments and blank lines.

### Objectives
Volume of coding activity: Although code changes can be a proxy to the coding
activity of a project, not all changes are the same. Considering the aggregated
number of lines touched in all changes gives a complementary idea of how large
the changes are, and in general, how large is the volume of coding activity.

#### Visualizations

#### Steps

1. Click on the `Visualize` option in the sidebar and click on `+` to pick your
   visualization type. Choose `Area` as visualization type.

2. Select `git` as index.

3. For `Metrics`, we'll need to add 2 of them, that is two `Y-axis`. For the
   first one set the y-axis aggregation to `Sum` and field to `lines_added`. Set
   `Lines added` for the custom label. For the 2nd Y-axis, set the aggregation
   to `Sum` and field to `painless_inverted_lines_removed_git`. Set the custom
   label to `Lines removed`.

   ![metrics lines added](../assets/metrics_code_lines_1.png)

   ![metrics lines removed](../assets/metrics_lines_removed.png)

4. For `Buckets`, pick the bucket type of `X-axis`.

5. Set the aggregation to `Date Histogram` and field to `grimoire_creation_date`
   and interval to `Auto`. Set `Time` for the custom label.

   ![bucket code lines](../assets/bucket_code_lines.png)

6. In the end, your visualization should like the following,

![code lines](../assets/code_lines.png)