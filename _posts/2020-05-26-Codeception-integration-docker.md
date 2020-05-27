---
layout: default
title: "Codeception and webdriver integration"
tags: [codeception, selenium, chromedriver, docker, acceptance-tests, tests]
date: 2020-05-26
time: 11:24
---
# Codeception and webdriver integration

Just some notes

## Install codeception
 
- Composer:
```
composer require codeception/codeception --dev
```

- Codecept bootrstrap:
```
call vendor/bin/codecept bootstrap
```

## Codeception vs docker setup
If running from docker use container's name in config.

 Set projects url in tests/acceptance.suite.yml: 
```
actor: AcceptanceTester
modules:
    enabled:
        - WebDriver:
            url: http://front -- "front" as docker service name
            host: selenium    -- "selenium" as docker service name
            browser: chrome
        - \Helper\Acceptance
    step_decorators: ~
extensions:
    enabled:
        - Codeception\Extension\Recorder:
              delete_successful: false
              delete_orphaned: true
              include_microseconds: true

```

Project docker file example:
```
services:
  front:
    image: front
    build:
      context: .
      target: front_dev
      dockerfile: ./docker/Dockerfile
    ports:
      - "4005:80"
  selenium:
    image: selenium/standalone-chrome
    ports:
      - "4444:4444"
    expose:
      - 4444
```
## Some cmd notes
Create first test:
```
codecept g:cest acceptance First
```
Run codeception test from outside of docker container:
-w /var/www/ - set up a docker working directory 
```
 docker exec -w /var/www/ -it front php /var/www/codecept.phar run -vvv --no-redirect
```