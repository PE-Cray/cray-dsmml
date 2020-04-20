dsmml_get_version_info
======================

::

   Retrieve DSMML major and minor version information

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_get_version_info(int *major, int *minor);

Arguments
---------

::

   major   major version information returned
   minor   minor version information returned

Description
-----------

::

   dsmml_get_version_info returns the major and minor version information
   from the DSMML library. This is a thread-safe query operation and it can
   used before the DSMML library initialization.

Return Values
-------------

::

   DSMML_RC_SUCCESS            successfully retrieved version information
   DSMML_RC_FAILURE            Unable to retrive version information
