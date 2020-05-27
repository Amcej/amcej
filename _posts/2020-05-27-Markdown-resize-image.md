---
layout: default
title: "Markdown resize images"
tags: [markdown, image, resize, kramdown]
date: 2020-05-27
time: 11:39
---
# Markdown resize images
*Just some notes*
using kramdown: [https://kramdown.gettalong.org/quickref.html](https://kramdown.gettalong.org/quickref.html)
You may addd {:class=""}
I like {:width="400px"}

If you are using kramdown try this to resize images:
```
![test image size](/assets/images/phpstorm-watcher-setup.png){:class="img-responsive"}
```
![test image size](/assets/images/phpstorm-watcher-setup.png){:class="img-responsive"}
```
![test image size](/assets/images/phpstorm-watcher-setup.png){:height="50%" width="50%"}
```
![test image size](/assets/images/phpstorm-watcher-setup.png){:height="50%" width="50%"}
```
![test image size](/assets/images/phpstorm-watcher-setup.png){:height="200px" width="400px"}
```
![test image size](/assets/images/phpstorm-watcher-setup.png){:height="200px" width="400px"}
```
![test image size](/assets/images/phpstorm-watcher-setup.png){: width="400px"}
```
![test image size](/assets/images/phpstorm-watcher-setup.png){:width="400px"}