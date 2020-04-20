dsmml_get_sheap_seg
===================

::

   Retrieve segment information using segment_id as input

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_get_sheap_seg(int segment_id, dsmml_sheap_seg_info_t **seg_info_attr);

Arguments
---------

::

   segment_id          segment id passed as input
   seg_info_attrs      output argument to retrieve the segment information

Description
-----------

::

   dsmml_get_sheap_seg is used to receive segment information incase the top
   level library requires it after the segment creation. Clients have to
   provide the segment id as input to retrieve segment information

Return Values
-------------

::

   DSMML_RC_SUCCESS            segment info successfully retrieved
   DSMML_RC_INVALID_PARAM      invalid segment ID passed or op_seg not NULL
   DSMML_RC_RESOURCE_ERROR     no segment is created with this ID or no
                               segments are created before

Notes
-----

::

   Refer dsmml_sheap_seg_info_t(3)
