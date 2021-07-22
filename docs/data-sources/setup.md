---
layout: default
title: setup.cfg
nav_order: 3
parent: Data sources
---

# What is setup.cfg ?

The setup file holds the configuration to arrange all process underlying GrimoireLab.

It is composed of sections which allow to define the general settings such as which phases to activate (e.g., collection, enrichment) and where to store the logs, as well as the location and credentials for SortingHat and the ElasticSearch instances where the raw and enriched data is stored. Furthermore, it also includes backend sections to set up the parameters used by Perceval to access the software development tools (e.g., GitHub tokens, gerrit username) and fetch their data.
