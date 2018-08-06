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

.. highlight:: js
  :linenothreshold:: 3
  GET  /api/lists

Request Format
^^^^^^^^^^^^^^

Response Format
^^^^^^^^^^^^^^^

List
-----

Retrieve a list based on the id.

Endpoint
^^^^^^^^

``GET  /api/lists/list_id``

Request Format
^^^^^^^^^^^^^^

Response Format
^^^^^^^^^^^^^^^

Yearly list
------------

Retrieve a yearly list based on the id of the list it belongs and the year.

Endpoint
^^^^^^^^

``GET  /api/lists/list_id/year``

Request Format
^^^^^^^^^^^^^^

Response Format
^^^^^^^^^^^^^^^

List categories
---------------

Retrieve all the available list categories.

Endpoint
^^^^^^^^

``GET  /api/categories``

Request Format
^^^^^^^^^^^^^^

Response Format
^^^^^^^^^^^^^^^

Affiliates
----------

Retrieve all the available affiliates.

Endpoint
^^^^^^^^

``GET  /api/affiliates``

Request Format
^^^^^^^^^^^^^^

Response Format
^^^^^^^^^^^^^^^
