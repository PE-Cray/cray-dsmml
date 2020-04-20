dsmml_init_ssheap_seg
=====================

::

   Initialize the segment which was previously created as a shared symmetric
   heap segment and share with other processes

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_init_ssheap_seg(int segment_id);

Arguments
---------

::

   segment_id   segment id

Description
-----------

::

   Initializes the segment which was previously created as a shared symmetric
   heap segment using the dsmml_create_ssheap_seg(3) operation and shared with
   other processes using dsmml_share_ssheap_seg(3) operation. To process
   this operation, all clients has to make sure that the segment is created
   in all processes and are shared between them. Hence, a barrier-like
   operation is required before calling this routine.

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

Notes
-----

::

   Refer dsmml_create_ssheap_seg(3), dsmml_share_ssheap_seg(3)
