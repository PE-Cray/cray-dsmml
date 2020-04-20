dsmml_sheap_free
================

::

   Free previously created memory allocation

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_sheap_free(int segment_id, void **ptr);

Arguments
---------

::

   segment_id      segment id as input
   ptr             pointer to previously created memory allocation

Description
-----------

::

   dsmml_sheap_free is ued to free previously created memory allocation

Return Values
-------------

::

   DSMML_RC_SUCCESS            memory successfully freed
   DSMML_RC_INVALID_PARAM      requested memory not previously allocated
   DSMML_RC_RESOURCE_ERROR     invalid segment ID passed

Notes
-----

::

   None.
