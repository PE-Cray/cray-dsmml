dsmml_finalize
==============

::

   Finalize and destroy all the segments created if the number of
   initializations is matched.

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_finalize(void);

Arguments
---------

::

   None.

Description
-----------

::

   Finalize function, used to destroy all created segments in the DSMML
   library. Operation is performed only when the number of initializations
   matches the finalize calls.

Return Values
-------------

::

   DSMML_RC_SUCCESS    either all segments destroyed or init count reduced
   DSMML_RC_FAILURE    no initialization previously found

Notes
-----

::

   None.
