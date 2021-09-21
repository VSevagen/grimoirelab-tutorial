---
layout: default
title: Contributor Diversity
nav_order: 3
parent: Understand personal engagement
grand_parent: Understanding Community Health
---

# Contributor Diversity
Question: What is the organizational diversity of contributions?

Organizational diversity expresses how many different organizations are involved in a project and how involved different organizations are compared to one another.

### Objectives
- Get a list of organizations contributing to a project.
- See the percentage of contributions from each organization within a defined period of time.
- See the change of composition of organizations within a defined period of time.
- Get a list of people that are associated with each organization.

### Implementation

* Collect data from data sources where contributions occur.
* Identify contributor affiliations to get a good estimate of which organizations they belong to.
* Correlate information about contributions, assigning each to appropriate organization.
* Depending on the needs of the project, you may want to consider such issues as how to handle multiple email addresses, affiliation changes over time, or contractor vs. employee.

### Visualization

* Add a sample visualization to any GrimoreLab Kibiter dashboard following these instructions:
    * Create a new Pie chart
      * Select the `all_onion` index
      * Metrics Slice Size: `Sum` Aggregation, `contributions` Field, `Contributions` Custom Label
      * Buckets Split Slices: `Terms` Aggregation, `author_or_name` Field, `metric: Contributions` Order By, `Descending` Order, `500` Size, `Organization` Custom Label
    * Example Screenshot

    ![Organizational Diversity Pie Chart](../assets/organizational-diversity_piechart.png)