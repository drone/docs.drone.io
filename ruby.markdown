---
layout: default
title: Ruby
icon: ruby
tagline: Building Ruby Projects
---

The following Node.js versions are available to your build:

* Ruby 1.8.7
* Node 1.9.3

Please note that Ruby versions are managed using [RVM](https://rvm.io/).

### Dependencies

The following dependency management tools are available:

* bundler
* rubygems

By default, your Ruby project is configured to management dependencies using
**Bundler**:

```
bundle install
```

### Testing

By default, your Ruby project is configured to execute test using **Rake**:

```
bundle exec rake
```
