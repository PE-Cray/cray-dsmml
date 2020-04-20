dsmml_create_sheap_seg
======================

::

   Create and initialize symmetric heap segment

Synopsis
--------

.. code:: bash

   dsmml_return_t dsmml_create_sheap_seg(dsmml_sheap_seg_info_t *seg_attrs);

Arguments
---------

::

   seg_attrs   input segment information attributes

Description
-----------

::

   Create amd initialize the symmetric heap segment based on the user input
   arguments. Users are expected to pass various memory information like the
   base address (virtual address space), length of the segment, memory type,
   pagesize, and mode information throught the dsmml_sheap_seg_info_t(3).

   Information on using the combination of the different types of memory and
   mode of allocation.

   Memory Types:
   DSMML_MEM_SYS_DEFAULT
   DSMML_MEM_NORMAL
   DSMML_MEM_FAST

   Different Modes:
   DSMML_MODE_DEFAULT
   DSMML_MODE_PREFERRED
   DSMML_MODE_BIND
   DSMML_MODE_INTERLEAVE


   Effect of using different combinations of memory types and modes of allocation:
                           DSMML_MEM_SYS_DEFAULT   DSMML_MEM_NORMAL    DSMML_MEM_FAST
   DSMML_MODE_DEFAULT             NO EFFECT        NO EFFECT           NO EFFECT
   DSMML_MODE_PREFERRED           NO EFFECT        DDR + MPOL_PREF     HBM + MPOL_PREF
   DSMML_MODE_BIND                NO EFFECT        DDR + MPOL_BIND     HBM + MPOL_BIND
   DSMML_MODE_INTERLEAVE          NO EFFECT        MPOL_INTERLEAVE     MPOL_INTERLEAVE

Return Values
-------------

::

   DSMML_RC_SUCCESS            segment successfully created
   DSMML_RC_INVALID_PARAM      invalid parameter like NULL pointer passed
   DSMML_RC_RESOURCE_ERROR     unavailable memkind or hugepage size requested
   DSMML_RC_NO_MEMORY          heap memory cannot be mapped or heap too huge
   DSMML_RC_UNKNOWN_FAIL       unknown error
   DSMML_RC_MEM_CORRUPT        saw memory corruption on segment during alloc

Notes
-----

::

   Refer dsmml_sheap_seg_info_t(3)
