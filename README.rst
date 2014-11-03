Django jQuery
=============


Requirements
------------

`Django <https://www.djangoproject.com/>`_ 1.3 or later


Installation
------------

::

    $ pip install -e git://github.com/Haos616/django-static-jquery.git@#egg=MyProject
Setup
-----

Just add ``'django.contrib.staticfiles'`` and ``'jquery'`` to INSTALLED_APPS in
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

    {{ STATIC_URL }}static_jquery/js/jquery.js


Admin template customization::

    {% extends "admin/base_site.html" %}

    {% block extrahead %}
        <script type="text/javascript" src="{{ STATIC_URL }}static_jquery/js/jquery.js" />
    {% endblock %}

Static files:

    static_jquery/js/jquery.js - JQuery - v1.11.1
    static_jquery/js/jquery.min.js - JQuery (min) - v1.11.1
    static_jquery/js/jquery.min.map - JQuery (map) - v1.11.1

    static_jquery/js/jquery-migrate.js - jQuery Migrate - v1.2.1
    static_jquery/js/jquery-migrate.min.js - jQuery Migrate (min) - v1.2.1