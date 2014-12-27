Django jQuery
=============

`JQuery <http://jquery.com/>`_ 2.1.3

Requirements
------------

`Django <https://www.djangoproject.com/>`_ 1.4 or later

Installation
------------

::

    $ pip install django-static-jquery==2.1.3

Setup
-----

Just add ``'django.contrib.staticfiles'`` and ``'django_static_jquery'`` to INSTALLED_APPS in
your settings.py::

    INSTALLED_APPS = (
        # ...

        'django.contrib.staticfiles',
        'django_static_jquery',

        # ...
    )

Refer to Django `static files <https://docs.djangoproject.com/en/dev/howto/static-files/>`_
documentation to configure and deploy static files.


Usage
-----

You can refer to jquery in your template with::

    {% load staticfiles %}
    {% static 'static_jquery/js/jquery.js' %}

Admin template customization::

    {% load staticfiles %}

    {% extends "admin/base_site.html" %}

    {% block extrahead %}
        <script type="text/javascript" src="{% static 'static_jquery/js/jquery.js' %}" />
    {% endblock %}

Static files::

    static_jquery/js/jquery.js - JQuery - v2.1.3
    static_jquery/js/jquery.min.js - JQuery (min) - v2.1.3
    static_jquery/js/jquery.min.map - JQuery (map) - v2.1.3

    static_jquery/js/jquery-migrate.js - jQuery Migrate - v1.2.1
    static_jquery/js/jquery-migrate.min.js - jQuery Migrate (min) - v1.2.1
