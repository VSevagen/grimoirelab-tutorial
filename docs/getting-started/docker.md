---
layout: default
title: Using docker
nav_order: 1
parent: Set up GrimoireLab
grand_parent: Getting-started
---

# Using docker

### Requirements

- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Docker](https://docs.docker.com/engine/install/)
- 2 CPUs, 8GB memory RAM

You can check whether you have everything installed through the following commands

```
$ git --version
$ docker --version
```

### Procedure

- Clone the GrimoireLab repo and change directory into <code>grimoirelab</code>

```
$ git clone https://github.com/chaoss/grimoirelab
$ cd grimoirelab
```

- Run the following command

```
$ docker run -p 127.0.0.1:5601:5601 \
-v $(pwd)/default-grimoirelab-settings/projects.json:/projects.json \
-v $(pwd)/default-grimoirelab-settings/setup.cfg:/setup.cfg \
-t grimoirelab/full
```

Your dashboard will be ready after a while at <code>http://localhost:5601</code>.
You can find more details about the docker based installation [here](https://github.com/chaoss/grimoirelab/tree/master/docker)
