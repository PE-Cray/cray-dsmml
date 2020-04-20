dsmml_sheap_realloc
===================

::

   Reallocate memory on the given segment

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_sheap_realloc(int segment_id, void **alloc_ptr, size_t length,
                                      void **realloc_ptr);

Arguments
---------

::

   segment_id      segment as input
   alloc_ptr       pointer to the previously allocated memory
   length          length of the new reallocated memory
   realloc_ptr     output pointer to the reallocated memory

Description
-----------

::

   Reallocate memory on a given segment over the already allocated memory.

Return Values
-------------

::

   DSMML_RC_SUCCESS            memory successfully reallocated
   DSMML_RC_NO_MEMORY          requested memory greater than available
   DSMML_RC_RESOURCE_ERROR     invalid segment ID passed
   DSMML_RC_INVALID_PARAM      invalid allocation paramter passed

Notes
-----

::

   None.
