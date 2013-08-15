---
layout: default
title: Python
tagline: Building Python Projects
icon: python
---

The following Python versions are available to your build:

 * Python 2.7
 * Python 3.2
 * Python 3.3

Please note that Python builds are executed inside a virtualenv instance.

## Dependencies

The following Python dependency management tools are pre-installed:

* setuptools
* easy_install
* pip

## Testing

The following Python testing frameworks are pre-installed:

* nose
* pytest

--------------------------------------------------------------------------------

## Examples

### Example 1

Example build script using pip for dependency management and nosetests for
unit testing:

```
pip install -r requirements.txt --use-mirrors
nosetests
```

### Example 2

Example build script using setuptools for dependency management and unit tests:

```
python setup.py install
python setup.py test
```

### Example 3

Using a traditional make file:

```
make test
```
