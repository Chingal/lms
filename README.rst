Manage Tickets
=================
Create an api rest that allows us to manage the transaction creation tickets in a upload application.

Api Root
========
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
  
Obtain Auth Token
=================

* **URL**: ``/api-token-auth/``

* **METHOD**: ``POST``

* **DATA PARAMS**: ``{"username": admin, "password": "********" }``
    
* **Success Response**:
    * **Code**: ``200 OK``
    * **Content**:

.. code-block:: python

	{"token": "xxxxxxx-12345-aaaa-bbbb-9876-xxxx"}


List Tickets
============

* **URL**: ``/api/tickets/``

* **METHOD**: ``GET``

* **Header** *(Authorization)* : *Token* `A` ``xxxxxxx-12345-aaaa-bbbb-9876-xxxx``
    
* **Success Response**:
    * **Code**: ``200 OK``
    * **Content**:

.. code-block:: python

	{"token": "xxxxxxx-12345-aaaa-bbbb-9876-xxxx"}




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
