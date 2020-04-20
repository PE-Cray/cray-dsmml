dsmml_sheap_seg_list_t
======================

::

   structure for getting all the created symmetric heaps as linked list

Synopsis
--------

.. code:: bash

   typedef struct dsmml_sheap_seg_list {
       struct dsmml_sheap_seg_list *next;
       dsmml_sheap_seg_info_t *     segment;
   } dsmml_sheap_seg_list_t;

Members
-------

::

   next        next segment in the linked list
   segment     pointer with the segment information

Notes
-----

::

   Refer dsmml_sheap_seg_info_t(3), and dsmml_get_sheap_seg_list(3)
