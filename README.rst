Manage Tickets
=================
Create an api rest that allows us to manage the transaction creation tickets in a upload application.

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
  
Obtain Auth Token
=================

A Django App that adds CORS (Cross-Origin Resource Sharing) headers to
responses.


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
