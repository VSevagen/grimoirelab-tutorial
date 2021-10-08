---
layout: default
title: Contributor Location
nav_order: 2
parent: Understand personal engagement
grand_parent: Understanding Community Health
---

# Contributor Location
Question: What is the location of contributors?

Geographical location from which contributors contribute, where they live, or
where they work.

### Objectives
To determine global locations of contributors in an effort to understand work
practices and times zones. To identify where contributions do not come from in
an effort to improve engagement in these areas.


### Visualizations

#### Dot Density Map

#### Steps

1. For `Metrics`, set the aggregation to `Count`. For `Buckets` set the geo coordinates.

  ![metrics geolocation](../assets/metrics_geolocation.png)

2. Set the aggregation to `GeoHash` and field to `user_geolocation`. Check the
   boxes related to precision, markets and request data.

   ![buckets georlocation](../assets/buckets_geolocation.png)

   ![geolcoation](../assets/geolocation.png)