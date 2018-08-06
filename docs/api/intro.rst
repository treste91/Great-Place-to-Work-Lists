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

**GET  /api/lists**

List
-----

Retrieve a list based on the id.

**GET  /api/lists/list_id**

Yearly list
------------

Retrieve a yearly list based on the id of the list it belongs and the year.

**GET  /api/lists/list_id/year**

List categories
---------------

Retrieve all the available list categories.

**GET  /api/categories**

Affiliates
----------

Retrieve all the available affiliates.

**GET  /api/affiliates**
