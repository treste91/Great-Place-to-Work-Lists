Introduction
============

The Great Place to Work REST API enables second and third party applications to access and manage *Lists*, *Yearly lists*, *List categories* and *Affiliates*.

API Authorisation
=================

Each request to the Great Place to Work REST API must include a valid **username** and **password** as GET parameters.

Endpoints
=========

The available endpoints are:

* **Lists**
* **List**
* **Yearly list**
* **List categories**
* **Affiliates**

Lists
-----

Retrieve all the available lists.

Endpoint
^^^^^^^^

.. code-block:: text
  
    GET  /api/lists

Request Format
^^^^^^^^^^^^^^

You must set an Accept: application/json header on all requests.

Example:

.. code-block:: text

    http://localhost/api/lists/?username=test&password=test

Response Format
^^^^^^^^^^^^^^^

.. code-block:: text

    {
    "success": true,
    "message": null,
    "messages": null,
    "data": [
        {
            "id": "3",
            "name_eng": "List_3",
            "description_eng": "Description of List_3",
            "category_id": "1",
            "owned_by_affiliate_id": "3",
            "ordering": "3",
            "state": "1",
            "category": "Category_1",
            "yearly_list_publication_date": {
                "date": "2018-05-02 00:00:00.000000",
                "timezone_type": 2,
                "timezone": "GMT"
            },
            "yearly_list_id": "6",
            "yearly_list_banner_image": "https://www.greatplacetowork.com/images/list-headers/2017smb-crop_gptw_homepageALT_1600x606.png",
            "yearly_list_logo_url_eng": "https://www.greatplacetowork.com/images/logos/2018-Best-Workplaces-in-Technology.png",
            "yearly_list_year": "2018"
        },
        {
            "id": "2",
            "name_eng": "List_2",
            "description_eng": "Description of List_2",
            "category_id": "2",
            "owned_by_affiliate_id": "2",
            "ordering": "2",
            "state": "1",
            "category": "Category_2",
            "yearly_list_publication_date": {
                "date": "2018-04-22 00:00:00.000000",
                "timezone_type": 2,
                "timezone": "GMT"
            },
            "yearly_list_id": "2",
            "yearly_list_banner_image": "https://www.greatplacetowork.com/images/list-headers/2017smb-crop_gptw_homepageALT_1600x606.png",
            "yearly_list_logo_url_eng": "https://www.greatplacetowork.com/images/logos/2018-Best-Workplaces-in-Technology.png",
            "yearly_list_year": "2018"
        },
        {
            "id": "1",
            "name_eng": "List_1",
            "description_eng": "Description of List_1",
            "category_id": "1",
            "owned_by_affiliate_id": "1",
            "ordering": "1",
            "state": "1",
            "category": "Category_1",
            "yearly_list_publication_date": {
                "date": "2018-04-21 00:00:00.000000",
                "timezone_type": 2,
                "timezone": "GMT"
            },
            "yearly_list_id": "1",
            "yearly_list_banner_image": "https://s3.amazonaws.com/media.greatplacetowork.com/images/BLANK_Homepage_Retail_List_3.2gptw_homepage_1600x606.jpg",
            "yearly_list_logo_url_eng": "https://www.greatplacetowork.com/images/logos/2018-Best-Workplaces-in-Technology.png",
            "yearly_list_year": "2018"
        }
    ]
}

List
-----

Retrieve a list based on the id.

Endpoint
^^^^^^^^

.. code-block:: text
  
    GET  /api/lists/list_id

Request Format
^^^^^^^^^^^^^^

You must set an Accept: application/json header on all requests.

Example:

.. code-block:: text

    http://localhost/api/lists/1/?username=test&password=test

Response Format
^^^^^^^^^^^^^^^

.. code-block:: text

Yearly list
------------

Retrieve a yearly list based on the id of the list it belongs and the year.

Endpoint
^^^^^^^^

.. code-block:: text
  
    GET  /api/lists/list_id/year

Request Format
^^^^^^^^^^^^^^

You must set an Accept: application/json header on all requests.

Response Format
^^^^^^^^^^^^^^^

.. code-block:: text

List categories
---------------

Retrieve all the available list categories.

Endpoint
^^^^^^^^

.. code-block:: text
  
    GET  /api/categories

Request Format
^^^^^^^^^^^^^^

You must set an Accept: application/json header on all requests.

Response Format
^^^^^^^^^^^^^^^

.. code-block:: text

Affiliates
----------

Retrieve all the available affiliates.

Endpoint
^^^^^^^^

.. code-block:: text
  
    GET  /api/affiliates

Request Format
^^^^^^^^^^^^^^

You must set an Accept: application/json header on all requests.

Response Format
^^^^^^^^^^^^^^^

.. code-block:: text
