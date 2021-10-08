---
layout: default
title: Contributors
nav_order: 1
parent: Understand personal engagement
grand_parent: Understanding Community Health
---

# Contributors
Question: Who are the contributors to a project?

A contributor is defined as anyone who contributes to the project in any way.
This metric ensures that all types of contributions are fully recognized in the
project.

### Objectives
Open source projects are comprised of a number of different contributors.
Recognizing all contributors to a project is important in knowing who is helping
with such activities as code development, event planning, and marketing efforts.

### Visualizations

### List of contributor names (often with information about their level of engagement)

#### Steps

1. For `Metrics`, set the aggregation to `Count` and `Buckets` to `Terms`. Set
   the field in buckets to `author_name`. Set the order to either descending or
   ascending depending on your preference.

   ![metrics contributor](../assets/metrics_contributors.png)

   ![buckets contributor](../assets/buckets_contributors.png)

   ![contributors](../assets/contributors.png)

2. You can also some more metrics to see the sum of lines removes, sum of lines
   added or the number of projects contributor is involved into.

3. For the number of projects involved, click on `Add metrics`. Set the
   aggregation to `Unique Count` and field to `project`. 
   
   ![metrics project count](../assets/metrics_project_count.png)

   ![contributor project](../assets/contributor_projects.png)

4. For the sum of lines added, click on `Add metrics`. Set the aggregation to
   `Sum` and field to `lines_added`.

   ![metrics line added](../assets/metrics_line_added.png)

   ![contributor line added](../assets/contributor_lines_added.png)

5. For sum of lines removes, click on `Add metrics`. Set the aggregation to
   `Sum` and field to `lines_removed`.

   ![metrics lines removed](../assets/metrics_lines_removed.png)

   ![contributor lines removed](../assets/contributor_lines_removed.png)

### Summary number of contributors

#### Steps

1. For `metrics`, set the aggregation to `Unique Count` and the field to `author_uuid`. 

    ![metrics](../assets/metrics_contributor_number.png)

2. This metric requires no changes in the `Buckets`.

    ![Summary number of contributors](../assets/contributor_number.png)

3. Change in the number of active contributors over time

![Contributor growth](../assets/contributors_growth.png)

#### New contributors

#### Steps

1. For `metrics`, set the aggregation to `Min` and field to `grimoire_creation_date`.

    ![metrics newcomers](../assets/metrics_newcomers.png)

2. For `Buckets`, click on `Split rows` and set the aggregation to `Terms` and
   field to `author_name`. Set the order to either descending or ascending based
   on your preference.

   ![buckets newcomers](../assets/buckets_newcomers.png)

![New contributors](../assets/newcomers.png)