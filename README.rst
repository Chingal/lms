Api Root
--------
* **URL**: ``/api/``

* **METHOD**: ``GET``

* **Success Response**:
    * **Code**: ``200 OK``
    * **Content**:

.. code-block:: javascrip

	{   
    		"tickets": "http://localhost:8000/api/tickets/",
    		"files": "http://localhost:8000/api/files/"
    	}
``CsrfViewMiddleware``
  
ENDPOINTS
===================

A Django App that adds CORS (Cross-Origin Resource Sharing) headers to
responses.

Although JSON-P is useful, it is strictly limited to GET requests. CORS
builds on top of ``XmlHttpRequest`` to allow developers to make cross-domain
requests, similar to same-domain requests. Read more about it here:
http://www.html5rocks.com/en/tutorials/cors/

.. image:: https://travis-ci.org/ottoyiu/django-cors-headers.svg?branch=master
   :target: https://travis-ci.org/ottoyiu/django-cors-headers


Requirements
------------

Tested with all combinations of:

* Python: 2.7, 3.6
* Django: 1.8, 1.9, 1.10, 1.11, 2.0

Setup
-----

Install from **pip**:

.. code-block:: sh

    pip install django-cors-headers

and then add it to your installed apps:

.. code-block:: python

    INSTALLED_APPS = (
        ...
        'corsheaders',
        ...
    )
