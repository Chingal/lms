** Endpoint **
---
Api Root
---
* **URL: **  `/api/`

* **Method:** `GET`

* **Success Response:**
  * **Code:** 200 OK
  * **Content:**
    ```json
{
		"tickets": "http://localhost:8000/api/tickets/",
    	"files": "http://localhost:8000/api/files/"
}
    ```
---
Obtain Auth Token
---
* **URL: **  `/api-token-auth/`

* **Method:** `POST`

* **Data Params: **
```json
{"username": admin, "password": "********" }
    ```
* **Success Response:**
  * **Code:** 200 OK
  * **Content:**
    ```json
{"token": "xxxxxxx-12345-aaaa-bbbb-9876-xxxx"}
    ```
---
List Tickets
---
* **URL: **  `/api/tickets/`

* **Method:** `GET`

* **Headers: **
	* **Authorization *(Required)*: ** *Token* `xxxxxxx-12345-aaaa-bbbb-9876-xxxx`

* **URL Params Filter: ** `status`, `start_date`, `end_date`
```json
?status=PENDING
?start_date=2018-12-12
?end_date=2018-12-12
?start_date=2018-11-12&end_date=2018-12-12
    ```
* **Success Response:**
  * **Code:** 200 OK
  * **Content:**
    ```json
{
        "count": 3,
        "next": null,
        "previous": null,
        "results": [
            {
                "url": "http://localhost:8000/api/tickets/1/",
                "user": "admin",
                "limit": 5,
                "status": "PENDING",
                "files": [
                    {
                        "file": "/media/upload/admin/image1.png",
                        "ticket": 1
                    },
                    {
                        "file": "/media/upload/admin/image2.png",
                        "ticket": 1
                    }
                ]
            }
        ]
}
    ```
---
Create Ticket
---
* **URL: **  `/api/tickets/`

* **Method:** `POST`

* **Headers: **
	* **Authorization:** *Token* `xxxxxxx-12345-aaaa-bbbb-9876-xxxx`

* **Data Params: **
```json
{"limit": 5, "status": "PENDING"}
    ```
    * ** STATUS **:

	`PENDING`:  The user has not yet uploaded any image.
	`IN PROGRESS`: The user uploaded an image.
	`COMPLETED`: The user uploaded all the images.
* **Success Response:**
  * **Code:** 200 OK
  * **Content:**
    ```json
{
        "url": "http://localhost:8000/api/tickets/1/",
        "user": "admin",
        "limit": 5,
        "status": "PENDING",
        "files": []
}
    ```
---
Upload File
---
* **URL: **  `/api/files/`

* **Method:** `POST`

* **Headers: **
	* **Authorization:** *Token* `xxxxxxx-12345-aaaa-bbbb-9876-xxxx`

* **Data Params: **
```json
{"ticket": id, "file": "path"}
    ```
* **Success Response:**
  * **Code:** 200 OK
  * **Content:**
    ```json
{
    	"file": "/media/upload/admin/image1.png",
    	"ticket": id
}
    ```

