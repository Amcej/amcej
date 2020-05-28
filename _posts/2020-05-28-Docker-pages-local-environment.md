---
layout: default
title: "GitHub pages local development with Jekyll in Docker"
tags: [Jekyll, docker, github-pages]
date: 2020-05-28
time: 12:39
---
# GitHub pages local development with Jekyll in Docker
*Just some notes*
- want to see github pages changes before commiting
- jekyll serve example docker command:

```
docker run --rm --label=jekyll --volume=$YOUR_LOCAL_PATH:/srv/jekyll  -it -p 4000:4000 jekyll/jekyll jekyll serve

```

- profit on [http://localhost:4000](http://localhost:4000)
