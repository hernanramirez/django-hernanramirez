========================
django-hernanramirez
========================

![Django 1.8.2](http://img.shields.io/badge/Django-1.8.2-brightgreen.svg)
[![MIT License](https://img.shields.io/cocoapods/l/AFNetworking.svg)](http://opensource.org/licenses/MIT)

A simple personalized project template for Django 1.8.2 

Forked from the original [django-two-scoops-project](https://github.com/twoscoops/django-twoscoops-project)

To use this project follow these steps:

#. Create your working environment
#. Install Django
#. Create the new project using the django-hernanramirez template
#. Install additional dependencies

*note: these instructions show creation of a project called "PROJECT_NAME".  You
should replace this name with the actual name of your project.*


Working Environment
===================

You have several options in setting up your working environment.  We recommend
using virtualenv to separate the dependencies of your project from your system's
python environment.  If on Linux or Mac OS X, you can also use virtualenvwrapper to help manage multiple virtualenvs across different projects.

Virtualenv Only
---------------

First, make sure you are using virtualenv (http://www.virtualenv.org). Once
that's installed, create your virtualenv::

    $ virtualenv veen_PROJECT_NAME

You will also need to ensure that the virtualenv has the project directory
added to the path. Adding the project directory will allow `django-admin.py` to
be able to change settings using the `--settings` flag.

Virtualenv with virtualenvwrapper
------------------------------------

In Linux and Mac OSX, you can install virtualenvwrapper (http://virtualenvwrapper.readthedocs.org/en/latest/),
which will take care of managing your virtual environments and adding the
project path to the `site-directory` for you::

    $ mkdir PROJECT_NAME
    $ mkvirtualenv -a PROJECT_NAME PROJECT_NAME-dev
    $ cd PROJECT_NAME && add2virtualenv `pwd`

Using virtualenvwrapper with Windows
----------------------------------------

There is a special version of virtualenvwrapper for use with Windows (https://pypi.python.org/pypi/virtualenvwrapper-win).::

    > mkdir PROJECT_NAME
    > mkvirtualenv PROJECT_NAME-dev
    > add2virtualenv PROJECT_NAME


Installing Django
=================

To install Django in the new virtual environment, run the following command::

    $ pip install django

Creating your project
=====================

To create a new Django project called '**PROJECT_NAME**' using
django-hernanramirez, run the following command::

    $ django-admin.py startproject --template=https://github.com/hernanramirez/django-hernanramirez/archive/master.zip --extension=py,rst,html PROJECT_NAME_project


Installation of Dependencies
=============================

Depending on where you are installing dependencies:

In development::

    $ pip install -r requirements/local.txt

For production::

    $ pip install -r requirements.txt

*note: We install production requirements this way because many Platforms as a
Services expect a requirements.txt file in the root of projects.*


Acknowledgements
================

![Two Scoops of Django](http://twoscoops.smugmug.com/Two-Scoops-Press-Media-Kit/i-C8s5jkn/0/O/favicon-152.png "Two Scoops Logo")

This project follows best practices as espoused in [Two Scoops of Django: Best Practices for Django 1.6](http://twoscoopspress.org/products/two-scoops-of-django-1-6).
