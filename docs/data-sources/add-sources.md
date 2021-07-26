---
layout: default
title: Add data sources
nav_order: 3
parent: Data sources
---

# How to add a new data source

In order to add data sources, you need to do some changes in both <code>projects.json</code> and <code>setup.cfg</code>

For example, let's just say you want to analyze the commits of one particular project from your github repo.

##### projects.json

Check out the snippet below and do the same with your `projects.json` file. **Replace the information below with your own**.

```
{
    "VSevagen": {
        "git": [
            "https://github.com/VSevagen/CMS-Blog"
        ]
    }
}
```

##### setup.cfg

Check out the snippet below and do the same with your `setup.cfg` file.

```
[git]
raw_index = git_raw
enriched_index = git_enriched
latest-items = true (suggested)
studies = [enrich_demography:git, enrich_git_branches:git, enrich_areas_of_code:git, enrich_onion:git, enrich_extra_data:git] (optional)

[enrich_demography:git] (optional)

[enrich_git_branches:git] (optional)
run_month_days = [1, 23] (optional)

[enrich_areas_of_code:git] (optional)
in_index = git_raw
out_index = git-aoc_enriched

[enrich_onion:git] (optional)
in_index = git_enriched
out_index = git-onion_enriched

[enrich_forecast_activity]
out_index = git_study_forecast
```

Once you have made the following changes, just re-run your containers with docker-compose

```console
$ docker-compose up -d
```

Give it some time to gather the data and after a while your dashboard and data should be ready at `http://localhost:5601`.<br>

![dashboard](../assets/dashboard.png)

In the case you need to add another data source, refer to the [configuration](https://vsevagen.github.io/grimoirelab-tutorial/docs/data-sources/configurations/) section to know the exact changes to be ported to you projects.json and setup.cfg files
