# Brunch with js
This is a simple js skeleton for [Brunch](http://brunch.io/).

Main languages are JavaScript,
[Stylus](http://learnboost.github.com/stylus/) and
[Eco](https://github.com/sstephenson/eco).

## Getting started

Clone the repo and run `npm install` & `brunch build`.
More info at [official site](http://brunch.io)

## Overview

    config.coffee
    README.md
    /app/
      /assets/
        index.html
        humans.txt
        images/
      collections/
      models/
      styles/
      routers/
      templates/
      views/
      initialize.coffee
    /test/
      functional/
      unit/
    /vendor/
      scripts/
        backbone.js
        jquery.js
        console-helper.js
        underscore.js
      styles/
        normalize.css
        helpers.css

* `config.coffee` contains configuration of your app. You can set plugins /
languages that would be used here.
* `app/assets` contains images / static files. Contents of the directory would
be copied to `build/` without change.
Other `app/` directories could contain files that would be compiled. Languages,
that compile to JS (coffeescript, roy etc.) or js files and located in app are 
automatically wrapped in module closure so they can be loaded by 
`require('module/location')`.
* `test/` contains feature & unit tests.
* `vendor/` contains all third-party code. The code wouldn’t be wrapped in
modules, it would be loaded instantly instead.

This all will generate `public/` (by default) directory when `brunch build` or `brunch watch` is executed.
