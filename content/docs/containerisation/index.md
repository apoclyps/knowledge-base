---
title: "Containerisation"
date: 2019-02-11T19:27:37+10:00
weight: 6
summary: "Configure your terminal and themeing."
---

### Useful Docker Commands

Kill all running containers:

```bash
docker kill $(docker ps -q)
```

Delete all stopped containers:

```bash
docker rm $(docker ps -a -q)
```

Delete all images:

```bash
docker rmi $(docker images -q)
```

Delete all unused & unnamed images:

```bash
docker rmi -f $(docker images -f "dangling=true" -q)
```

Remove all containers with status=exited:

```bash
docker rm $(docker ps -q -f status=exited)
```

Stop all containers (will run stop only for active):

```bash
docker stop $(docker ps -q)
```

Stop all containers (will run stop only for all):

```bash
docker stop $(docker ps -aq)
```

Remove all dangling images:

```bash
docker rmi $(docker images --filter "dangling=true" -q --no-trunc) 2>/dev/null
```
