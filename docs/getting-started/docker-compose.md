---
layout: default
title: Using docker-compose
nav_order: 2
parent: Set up GrimoireLab
grand_parent: Getting-started
---

# Using docker-compose

GrimoireLab provides some configuration files to easily get started using docker-compose. It is also one of the easiest way to get started with GrimoireLab

### Requirements

- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Docker](https://docs.docker.com/engine/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- At least 8GB RAM, 2GB SWAP and 2 CPU's

You can check whether you have everything installed through the following commands

```
$ git --version
$ docker --version
$ docker-compose --version
```

### Procedure

- Clone the GrimoireLab repo and change directory into <code>docker-compose</code> folder.

```
$ git clone https://github.com/chaoss/grimoirelab
$ cd grimoirelab.docker-compose
```

- Set <code>vm.max_map_count</code> to at least 262144 to avoid out of memory exceptions

```
$ sysctl -w vm.max_map_count=262144
```

- Start GrimoireLab. If you run in a <strong>permission denied</strong> issue, run the the command below with <code>sudo</code>

```
$ docker-compose up -d
```

Once your container have successfully started, open <code>http://localhost:5601</code> on your browser

### Error handling

If you ever run into some issues, run <code>docker-compose up</code> without the <code>-d</code> flag. That will output all logs during the startup so you'll be able to identify the issue.
