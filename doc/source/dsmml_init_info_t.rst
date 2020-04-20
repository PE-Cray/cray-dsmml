dsmml_init_info
===============

::

   DSMML structure for passing initialization input arguments into the library

Synopsis
--------

.. code:: bash

   typedef struct dsmml_init_info {
       int     mype;
       int     smp_mype;
       int     smp_npes;
   } dsmml_init_info_t;

Members
-------

::

   mype        my PE index information
   smp_mype    my local PE index
   smp_npes    total number of local PEs

Notes
-----

::

   Refer dsmml_init(3)
