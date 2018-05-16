Manage Tickets
=================
Create an api rest that allows us to manage the transaction creation tickets in a upload application.

Api Root
========
* **URL**: ``/api-token-auth/``

* **METHOD**: ``POST``

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

* **URL**: ``/api/``

* **METHOD**: ``GET``

* **DATA PARAMS**: ``{"username": admin, "password": "********" }``
    
.. code-block:: javascrip

	{"username": admin, "password": "********" }

* **Success Response**:
    * **Code**: ``200 OK``
    * **Content**:

.. code-block:: javascrip

	{"token": "xxxxxxx-12345-aaaa-bbbb-9876-xxxx"}

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
