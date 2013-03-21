---
layout: default
title: Ruby
icon: ruby
tagline: Building Ruby Projects
---

The following Ruby versions are available to your build:

* Ruby 1.8.7-p370 
* Ruby 1.9.3-p385
* Ruby 2.0.0-p0

Please note that Ruby versions are managed using [rbenv](https://github.com/sstephenson/rbenv/).

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
