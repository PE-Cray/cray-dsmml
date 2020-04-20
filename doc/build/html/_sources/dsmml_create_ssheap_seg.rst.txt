dsmml_create_ssheap_seg
=======================

::

   Create shared symmetric heap segment

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_create_ssheap_seg(dsmml_sheap_seg_info_t *seg_attrs);

Arguments
---------

::

   seg_attrs   input segment information attributes

Description
-----------

::

   Creates shared symmetric heap segment based on the segment information
   attributes passed. While the shared symmetric heap segment is created
   after returning from this routine, to utilize this shared symmetric heap
   segment, users are required to share and initialize the segment using
   dsmml_share_ssheap_seg(3) and dsmml_init_ssheap_seg(3).

   Shared symmetric heap segments are usable only after being shared and
   initialized.

Return Values
-------------

::

   DSMML_RC_SUCCESS         - segment successfully initialized
   DSMML_RC_INVALID_PARAM   - invalid parameter like NULL pointer passed
   DSMML_RC_RESOURCE_ERROR  - unavailable memkind or hugepage size requested
   DSMML_RC_NO_MEMORY       - heap memory cannot be mapped or heap too huge
   DSMML_RC_UNKNOWN_FAIL    - unknown error
   DSMML_RC_MEM_CORRUPT     - saw memory corruption on segment during alloc
   DSMML_RC_UNKNOWN_FAIL    - unknown error

Notes
-----

::

   Refer dsmml_share_ssheap_seg(3), dsmml_init_ssheap_seg(3)
