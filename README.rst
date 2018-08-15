CPF Field to use in Django Model Form
=====================================
.. image:: https://travis-ci.org/silviolleite/cfp-field.svg?branch=master
    :target: https://travis-ci.org/silviolleite/cfp-field

.. image:: https://img.shields.io/pypi/v/python-decouple.svg
    :target: https://pypi.python.org/pypi/django-cpffield/
    :alt: Latest PyPI version


*cfp-field* This is a test implementatipon of the CPF Validation as part of
the "Mão na Massa" proposal of the 4th module of Welcome to the Django
training (http://welcometothedjango.com.br/).


Como instalar?
--------------

.. code-block:: console

    pip install django-cpffield


Add "cpffield" to your INSTALLED_APPS setting like this::

    INSTALLED_APPS = [
        ...
        'cpffield',
    ]

Como utilizar dentro de um model.py no django?
--------------------------------------------------
.. code-block:: python

    from django.db import models
    from cpffield import cpffield


    class MyModel(models.Model):
        cpf = cpffield.CPFField('CPF', max_length=14)

