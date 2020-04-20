dsmml_get_sheap_seg_list
========================

::

   Retrieve information of all the created segments are linked list

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_get_sheap_seg_list(dsmml_sheap_seg_list_t **seg);

Arguments
---------

::

   seg     output argument to retrieve the linked list of all created segments

Description
-----------

::

   Receive a linked list of all the available segments incase the top level
   library requires after creating the segment. This will return the starting
   element of the list and applications

Return Values
-------------

::

   DSMML_RC_SUCCESS            actual list pointer retrieved
   DSMML_RC_INVALID_PARAM      ip_seg passed is not NULL
   DSMML_RC_RESOURCE_ERROR     no segments are created before

Notes
-----

::

   Refer dsmml_sheap_seg_list_t(3)
