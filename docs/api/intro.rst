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

.. code-block:: json

    {
    "success": true,
    "message": null,
    "messages": null,
    "data": 
      [
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

.. code-block:: json

    {
    "success": true,
    "message": null,
    "messages": null,
    "data": 
      [
          {
              "id": "1",
              "name_eng": "List_1",
              "description_eng": "Description of List_1",
              "category_id": "1",
              "owned_by_affiliate_id": "1",
              "ordering": "1",
              "state": "1",
              "category_name": "Category_1"
          },
          {
              "id": "1",
              "list_id": "1",
              "year": "2018",
              "name_eng": "List_1_2018",
              "description_long_eng": "Description of List_1_2018",
              "logo_url_eng": "https://www.greatplacetowork.com/images/logos/2018-Best-Workplaces-in-Technology.png",
              "publish_date": "2018-04-21 00:00:00",
              "state": "1",
              "banner_image": "https://s3.amazonaws.com/media.greatplacetowork.com/images/BLANK_Homepage_Retail_List_3.2gptw_homepage_1600x606.jpg",
              "certified_by": "2018-04-21 00:00:00",
              "methodology_html": "html",
              "list_name": "List_1",
              "labeled_id": "1",
              "company_logo": "https://s3.amazonaws.com/culturesurvey.greatplacetowork.com/public/prd_logos_v11/L-QuickenLoans-RGB-20161123_calogo4090.jpg,https://s3.amazonaws.com/culturesurvey.greatplacetowork.com/public/prd_logos_v11/somclogo_calogo3701.jpg",
              "logos": [],
              "company_logos": [
                  "https://s3.amazonaws.com/culturesurvey.greatplacetowork.com/public/prd_logos_v11/L-QuickenLoans-RGB-20161123_calogo4090.jpg",
                  "https://s3.amazonaws.com/culturesurvey.greatplacetowork.com/public/prd_logos_v11/somclogo_calogo3701.jpg"
              ]
          }
        ]
     }

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

Example:

.. code-block:: text

    http://localhost/api/lists/1/2018/?username=test&password=test

Response Format
^^^^^^^^^^^^^^^

.. code-block:: json

    {
    "success": true,
    "message": null,
    "messages": null,
    "data": 
      [
          {
              "id": "1",
              "list_id": "1",
              "year": "2018",
              "name_eng": "List_1_2018",
              "description_long_eng": "Description of List_1_2018",
              "logo_url_eng": "https://www.greatplacetowork.com/images/logos/2018-Best-Workplaces-in-Technology.png",
              "publish_date": "2018-04-21 00:00:00",
              "state": "1",
              "banner_image": "https://s3.amazonaws.com/media.greatplacetowork.com/images/BLANK_Homepage_Retail_List_3.2gptw_homepage_1600x606.jpg",
              "certified_by": "2018-04-21 00:00:00",
              "methodology_html": "html",
              "list_name": "List_1"
          },
          [
              {
                  "label": "Label_1",
                  "id": "1",
                  "parent_company_id": null,
                  "salesforce_id": "100",
                  "cached_name_eng": "Company_1",
                  "industry_id": "18",
                  "location": "Thessaloniki, Greece",
                  "banner_image": "https://s3.amazonaws.com/culturesurvey.greatplacetowork.com/public/prd_photos_v11/RockConnections-20140408-1581_caphoto23773.jpg",
                  "logo_url_eng": "https://s3.amazonaws.com/culturesurvey.greatplacetowork.com/public/prd_logos_v11/L-QuickenLoans-RGB-20161123_calogo4090.jpg",
                  "company_url": "http://reviews.greatplacetowork.com/quicken-loans",
                  "labeled_yearly_list_id": "1",
                  "company_id": "1",
                  "company_quote_eng": "Quote for Company_1",
                  "rank": "1",
                  "industry_name": "Financial Services & Insurance"
              },
              {
                  "label": "Label_1",
                  "id": "2",
                  "parent_company_id": null,
                  "salesforce_id": "200",
                  "cached_name_eng": "Company_2",
                  "industry_id": "21",
                  "location": "Athens, Greece",
                  "banner_image": "https://s3.amazonaws.com/culturesurvey.greatplacetowork.com/public/prd_photos_v11/Registration_caphoto21366.jpg",
                  "logo_url_eng": "https://s3.amazonaws.com/culturesurvey.greatplacetowork.com/public/prd_logos_v11/somclogo_calogo3701.jpg",
                  "company_url": "http://reviews.greatplacetowork.com/southern-ohio-medical",
                  "labeled_yearly_list_id": "1",
                  "company_id": "2",
                  "company_quote_eng": "Quote for Company_2",
                  "rank": "2",
                  "industry_name": "Health Care"
              }
          ],
          [
              {
                  "id": "5",
                  "list_id": "1",
                  "year": "2017",
                  "name_eng": "List_1_2017",
                  "description_long_eng": "Description of List_1_2017",
                  "logo_url_eng": "https://s3.amazonaws.com/media.greatplacetowork.com/images/2017-technology_color.png",
                  "publish_date": "2018-05-07 00:00:00",
                  "state": "1",
                  "banner_image": "https://s3.amazonaws.com/media.greatplacetowork.com/images/Technology_crophomepage_1600x606_10.jpg",
                  "certified_by": "2018-05-08 00:00:00",
                  "methodology_html": "html",
                  "is_active": "0"
              },
              {
                  "id": "1",
                  "list_id": "1",
                  "year": "2018",
                  "name_eng": "List_1_2018",
                  "description_long_eng": "Description of List_1_2018",
                  "logo_url_eng": "https://www.greatplacetowork.com/images/logos/2018-Best-Workplaces-in-Technology.png",
                  "publish_date": "2018-04-21 00:00:00",
                  "state": "1",
                  "banner_image": "https://s3.amazonaws.com/media.greatplacetowork.com/images/BLANK_Homepage_Retail_List_3.2gptw_homepage_1600x606.jpg",
                  "certified_by": "2018-04-21 00:00:00",
                  "methodology_html": "html",
                  "is_active": "1"
              }
          ],
          [
              "Label_1"
          ],
          [
              {
                  "list_name": "List_1",
                  "id": "5",
                  "list_id": "1",
                  "year": "2017",
                  "name_eng": "List_1_2017",
                  "description_long_eng": "Description of List_1_2017",
                  "logo_url_eng": "https://s3.amazonaws.com/media.greatplacetowork.com/images/2017-technology_color.png",
                  "publish_date": "2018-05-07 00:00:00",
                  "state": "1",
                  "banner_image": "https://s3.amazonaws.com/media.greatplacetowork.com/images/Technology_crophomepage_1600x606_10.jpg",
                  "certified_by": "2018-05-08 00:00:00",
                  "methodology_html": "html"
              },
              {
                  "list_name": "List_2",
                  "id": "3",
                  "list_id": "2",
                  "year": "2017",
                  "name_eng": "List_2_2017",
                  "description_long_eng": "Description of List_2_2017",
                  "logo_url_eng": "https://s3.amazonaws.com/media.greatplacetowork.com/images/list_texas_rgb_color.png",
                  "publish_date": "2018-05-06 00:00:00",
                  "state": "1",
                  "banner_image": "https://s3.amazonaws.com/media.greatplacetowork.com/images/Texas-Image.jpg",
                  "certified_by": "2018-05-07 00:00:00",
                  "methodology_html": "html"
              },
              {
                  "list_name": "List_3",
                  "id": "6",
                  "list_id": "3",
                  "year": "2018",
                  "name_eng": "List_3_2018",
                  "description_long_eng": "Description of List_3_2018",
                  "logo_url_eng": "https://www.greatplacetowork.com/images/logos/2018-Best-Workplaces-in-Technology.png",
                  "publish_date": "2018-05-02 00:00:00",
                  "state": "1",
                  "banner_image": "https://www.greatplacetowork.com/images/list-headers/2017smb-crop_gptw_homepageALT_1600x606.png",
                  "certified_by": "2018-05-03 00:00:00",
                  "methodology_html": "html"
              }
          ]
        ]
      }

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

Example:

.. code-block:: text

    http://localhost/api/categories/?username=test&password=test

Response Format
^^^^^^^^^^^^^^^

.. code-block:: json

    {
    "success": true,
    "message": null,
    "messages": null,
    "data": 
      [
          {
              "id": "1",
              "name_eng": "Category_1",
              "ordering": "1"
          },
          {
              "id": "2",
              "name_eng": "Category_2",
              "ordering": "2"
          }
      ]
    }

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

Example:

.. code-block:: text

    http://localhost/api/affiliates/?username=test&password=test

Response Format
^^^^^^^^^^^^^^^

.. code-block:: json

    {
    "success": true,
    "message": null,
    "messages": null,
    "data": 
      [
          {
              "id": "1",
              "name": "Affiliate_1"
          },
          {
              "id": "2",
              "name": "Affiliate_2"
          },
          {
              "id": "3",
              "name": "Affiliate_3"
          },
          {
              "id": "4",
              "name": "Affiliate_4"
          }
      ]
    }
