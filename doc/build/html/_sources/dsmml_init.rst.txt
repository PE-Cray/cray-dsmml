dsmml_init
==========

::

   Initialization function to initialize the library and return either success
   or failure based on the input argument provided.

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_init(dsmml_init_info_t *init_attrs);

Arguments
---------

::

   init_attrs  dsmml_init_info_t structure with all the initialization
               attributes

Description
-----------

::

   Initialization function to initialize the library. Clients are expected to
   pass the setup arguments through dsmml_init_info_t(3) argument. Based on
   the status of the initialization, library returns the return code.

Return Values
-------------

::

   DSMML_RC_SUCCESS         initialization successful
   DSMML_RC_INVALID_PARAM   invalid input argument parameters
   DSMML_RC_NOOP            if already initialized

Notes
-----

::

   Refer dsmml_init_info_t(3) manpage for more information about the input
   arguments.
   Multiple initialization and finalization operations are allowed.
