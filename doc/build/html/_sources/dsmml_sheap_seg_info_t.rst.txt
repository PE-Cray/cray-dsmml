dsmml_sheap_seg_info
====================

::

   structure for creating and maintaining symmetric heap creation.

Synopsis
--------

.. code:: bash

   typedef struct dsmml_sheap_seg_info {
       int            id;
       void *         act_addr;
       void *         base_addr;
       size_t         length;
       dsmml_type_t   type;
       dsmml_hpsize_t pagesize;
       dsmml_mode_t   mode;
   } dsmml_sheap_seg_info_t;

Members
-------

::

   id              output segment id
   act_addr        actual address for all future use
   base_addr       base vaddr
   length          length of the segment
   type            memory type
   pagesize        hugepage size
   mode            allocation mode

Notes
-----

::

   Refer dsmml_sheap_seg_list_t(3), dsmml_get_sheap_seg(3), and
   dsmml_create_sheap_seg(3),
