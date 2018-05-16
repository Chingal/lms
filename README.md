** Gestión de Tickets [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) **

## Sinopsis

>Crear un api rest que nos permita gestionar los tickets de creación de transacciones en una aplicación de subida de fotos

## Hacer Migraciones de Cambios en los Models

> python manage.py makemigrations

## Realizar Migración a la base de datos de PITLU

> python manage.py migrate

## Servir Archivos Estaticos

> python manage.py collectstatic

## Correr el Servidor Local de Django
    
    python manage.py runserver

.. code-block:: python

    MIDDLEWARE = [  # Or MIDDLEWARE_CLASSES on Django < 1.10
        ...
        'corsheaders.middleware.CorsMiddleware',
        'django.middleware.common.CommonMiddleware',
        ...
    ]


 Endpoint
==============

Api Root
--------
**URL: **  `/api/`

* **Method:** `GET`
