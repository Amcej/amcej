---
layout: default
title: "PhpStorm tests watcher setup"
tags: [codeception, selenium, chromedriver, docker, acceptance-tests, tests]
date: 2020-05-27
time: 11:24
---
# PhpStorm tests watcher setup
*Just some notes*

Want to run all tests automatically on any change. Should be run on background in docker silently - we do not care about the tests :)

Want to run this CMD:
```
 docker exec -w /var/www/ front php /var/www/codecept.phar run -vvv --no-redirect
```

# Phpstorm watcher setting:

![phpstorm-watcher-setup.png](/assets/images/phpstorm-watcher-setup.png)


Do not use -it interactive option. Otherwise you get some strange [error](https://willi.am/blog/2016/08/08/docker-for-windows-interactive-sessions-in-mintty-git-bash/)!
```
 the input device is not a TTY. If you are using mintty, try prefixing the command with 'winpty'
```
