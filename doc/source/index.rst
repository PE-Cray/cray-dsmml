.. Cray DSMML documentation master file, created by
   sphinx-quickstart on Mon Apr 20 13:36:54 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Cray DSMML
==========

DSMML - Distributed Symmetric Memory Management Library

DSMML is a stand-alone memory management library for maintaining distributed 
shared symmetric memory heaps for top level PGAS languages and libraries like 
Coarray Fortran, UPC, and OpenSHMEM. DSMML allows user libraries to create 
multiple symmetric heaps and share information with other libraries. Through 
DSMML, we could extract interoperability between PGAS programming models.

Cray DSMML, is a proprietary product from Cray, a Hewlett Packard Enterprise
company. Cray OpenSHMEMX, a propreitary OpenSHMEM library implemetation from
Cray, a Hewlett Packard Enterprise company makes use of DSMML for its symmetric
memory management. 

.. toctree::
   :maxdepth: 1
   :hidden:
    
   overview
   envvar
   dsmml_init
   dsmml_finalize
   dsmml_get_version_info
   dsmml_create_sheap_seg
   dsmml_create_ssheap_seg
   dsmml_share_ssheap_seg
   dsmml_init_ssheap_seg
   dsmml_get_sheap_seg
   dsmml_get_sheap_seg_list
   dsmml_sheap_malloc
   dsmml_sheap_realloc
   dsmml_sheap_free
   dsmml_init_info_t
   dsmml_sheap_seg_info_t
   dsmml_sheap_seg_list_t
   bug 
