---
layout: default
title: Pick an index-pattern
nav_order: 2
parent: Create a new dashboard
grand_parent: Dashboard (Panel)
has_children: false
has_toc: false
---

# How to choose an index ?

Before we choose an index, we need to understand the meaning of an index.

**An index** refers to a collection of JSON documents related to a particular data source
(git, jenkins, slack, etc...). Every index will have an index-pattern that shows the
different attributes in an index. 

When creating your visualization, you will use fields from the index-pattern to set your
metrics and bucket and plot the, against each other to generate the visualization.

![index](../assets/index.png)