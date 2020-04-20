dsmml_sheap_malloc
==================

::

   Allocate memory from the given segment

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_sheap_malloc(int segment_id, size_t length, void **ptr);

Arguments
---------

::

   segment_id  segment id as input
   length      length of the memory to be allocated in bytes
   ptr         pointer to the allocated memory

Description
-----------

::

   dsmml_sheap_malloc is used to allocate memory from previously created segment

Return Values
-------------

::

   DSMML_RC_SUCCESS            memory successfully allocated
   DSMML_RC_INVALID_PARAM      invalid param passed ptr !- NULL, or segid neg
   DSMML_RC_NO_MEMORY          requested memory greater than available
   DSMML_RC_RESOURCE_ERROR     invalid segment ID passed
   DSMML_RC_UNKNOWN_FAIL       unknown error
   DSMML_RC_MEM_CORRUPT        saw memory corruption on segment during alloc

Notes
-----

::

   None.
