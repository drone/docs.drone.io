---
layout: default
title: PHP
icon: php01
tagline: Building PHP Projects
---

The virtual machine is pre-installed with PHP 5.4 (Zend Engine) and includes the
following extensions:

* bcmath
* bz2
* calendar
* Core
* curl
* ctype
* date
* dba
* dom
* ereg
* exif
* fileinfo
* filter
* ftp
* gd
* gettext
* hash
* iconv
* intl
* json
* libxml
* mbstring
* mcrypt
* mhash
* mysql
* openssl
* pcntl
* pcre
* pgsql
* Phar 
* posix
* readline
* Reflection
* session
* shmop
* SimpleXML
* soap
* sockets
* SPL
* sqlite
* standard
* sysvmsg
* sysvsem
* sysvshm
* tidy
* tokenizer 
* wddx
* xml
* xmlreader
* xmlwriter
* zip
* zlib

## Dependencies

Example using **pear**:

```
sudo pear channel-discover pear.amazonwebservices.com
sudo pear install aws/sdk
```

Example using **composer**:

```
composer install
```

Example using **pyrus**

```
pyrus install packagename
```

## Unit Test

By default, your PHP project is configured to execute tests with PHP Unit:

```
phpunit --coverage-text .
```


